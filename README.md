# Research-Project
Surgical trainees have to learn surgical skills before undergoing real surgeries. Knot-tying is one such process. It is a complex skill that is acquired through several hours of training. This process requires expert supervision for continuous feedback. This research aims to aid the assessment of the knot-tying skill with the help of modern Computer Vision techniques.
The understanding of a scene in the given setting can be achieved by analysis of Hand Gestures. The proposed pipeline includes Hand Detection, Hand Pose Estimation and Phase Recognition techniques. Several approaches for hand detection has been tested and compared side-by-side. It includes one-stage detectors like YOLO and SSD; and two-stage detectors like Mask r-cnn on the knot-tying data. Several pose estimation techniques like Convolutional Pose Machines and Hand Keypoint Detection in Single Images using Multiview Bootstrapping. It is followed by the gesture recognition task. The assessment is done on two knot-tying sequences forehand throw and backhand throw.

# Results
## YOLO
![Alt text](https://github.com/rockchik/Research-Project/blob/master/Yolo.jpg?raw=true "YOLO")
### Precision Recall Graphs for Object Detection
![Alt text](https://github.com/rockchik/Research-Project/blob/master/hand_l.png?raw=true "PrecisionRecall")
![Alt text](https://github.com/rockchik/Research-Project/blob/master/hand_r.png?raw=true "PrecisionRecall")
## MultiView Bootstraping on Backhand throw
![Alt text](https://github.com/rockchik/Research-Project/blob/master/bht_hand.PNG?raw=true "MB")
## MultiView Bootstraping on forehand throw
![Alt text](https://github.com/rockchik/Research-Project/blob/master/fht_hand.PNG?raw=true "MB")
## Convolutional Pose Machines for hands
![Alt text](https://github.com/rockchik/Research-Project/blob/master/fr_128.jpg?raw=true "MB")
![Alt text](https://github.com/rockchik/Research-Project/blob/master/fr_145.jpg?raw=true "MB1")
![Alt text](https://github.com/rockchik/Research-Project/blob/master/fr_150.jpg?raw=true "MB2")
![Alt text](https://github.com/rockchik/Research-Project/blob/master/fr_47.jpg?raw=true "MB3")
### Sample Convolutinal Pose Machines
![Alt text](https://github.com/rockchik/Research-Project/blob/master/sample_cpm.png?raw=true "MB4")


# Conclusion
Although, our proposed pipeline does not generalize well on the given data. The keypoint estimation techniques have shown the results on par with our expectations. The failure to detect hand on some frames resulted in failure of the keypoint estimations due to the very nature of our proposed pipeline. Performance of the employed algorithms can be improved by creating more data in a controlled environment.

## Discussion 
This research incorporates the use of Deep Learning techniques to achieve the results
over a similar domain. Many of the Deep Learning algorithms were designed for specific
puposes on works well on very specific dataset. For many tasks, the traditional Computer Vision Algorithms
works better.
Overall the knot-tying is a complex process and evaluation can be complicated too,
due to the occlusions present in the recorded data.

## Limitation
Generally, hand can take a lot of complex shapes, creating a lot of occlusions. Especially, when it comes to the knot-tying process.

• Although, the results obtained are promising, developing an end-to-end integrated system is a complex task.
• The results obtained are promising. However, there are still disparities in the results obtained by these algorithms especially the Object detection tasks.

# Future Work
## Keypoints
In our experiments, all the hand joints are initialized as the keypoints which makes the process harder to analyze. For the evaluation purposes, only the articulation of the index finger and thumb is needed for the main hand. The present state-of-the-art has been achieved by using depth-images for keyppoint estimation techniques. So, incorporating the use of depth images may further increase
the accuracy of keypoints.

## Bounding boxes
Many of the failures of our experiments are due to the failure of detection of bounding boxes. So, much of the focus of the future work should be on increasing the accuracy of the bounding boxes. The miss rate for the bounding boxes can be decreased significantly by creating high-quality annotations.
## Data
Secondly, to achieve the state-of-the-art results it is necessary to create a high-quality dataset. The dataset should be collected in a controlled environment and the data should be recorded by the expert surgeons. Additionally, multiple camera angles should be tested for keypoint estimation techniques.
## Analysis
The estimation of keypoints can be incorporated with the use of traditional methods like Optical flow to analyze the gestures of the hand.
Also, other approaches like matching correspondences in the video can be tested

