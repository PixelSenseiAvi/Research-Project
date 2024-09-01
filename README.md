# Evaluation of Knot-Tying Process Using Modern Computer Vision Techniques

## Overview

Surgical trainees must master complex skills like knot-tying through extensive training. This process demands expert supervision for effective feedback. Our research aims to enhance the assessment of knot-tying skills using modern computer vision techniques. By analyzing hand gestures, we propose a pipeline that includes Hand Detection, Hand Pose Estimation, and Phase Recognition. This study evaluates various hand detection and pose estimation approaches on knot-tying sequences.

## Proposed Pipeline

1. **Hand Detection**: We use YOLOv3, a trained model, to detect hands in the frame.
2. **Hand Pose Estimation**: We employ Convolutional Pose Machines (CPM) and Multiview Bootstrapping (CMU), both pretrained, for hand pose estimation.
3. **Optical Flow**: Keypoints are analyzed using Optical Flow to assess knot-tying phases, including forehand and backhand throws.

## Results

### YOLOv3

- **Detection**: 
  ![YOLOv3](https://github.com/rockchik/Research-Project/blob/master/Yolo.jpg?raw=true "YOLOv3")
- **Precision-Recall Graphs for Object Detection**:
  ![Precision Recall (Left)](https://github.com/rockchik/Research-Project/blob/master/hand_l.png?raw=true "Precision Recall (Left)")
  ![Precision Recall (Right)](https://github.com/rockchik/Research-Project/blob/master/hand_r.png?raw=true "Precision Recall (Right)")

### Multiview Bootstrapping

- **Backhand Throw**:
  ![Backhand Throw](https://github.com/rockchik/Research-Project/blob/master/bht_hand.PNG?raw=true "Backhand Throw")
- **Forehand Throw**:
  ![Forehand Throw](https://github.com/rockchik/Research-Project/blob/master/fht_hand.PNG?raw=true "Forehand Throw")

### Convolutional Pose Machines

- **Sample Images**:
  ![Pose 1](https://github.com/rockchik/Research-Project/blob/master/fr_128.jpg?raw=true "Pose 1")
  ![Pose 2](https://github.com/rockchik/Research-Project/blob/master/fr_145.jpg?raw=true "Pose 2")
  ![Pose 3](https://github.com/rockchik/Research-Project/blob/master/fr_150.jpg?raw=true "Pose 3")
  ![Pose 4](https://github.com/rockchik/Research-Project/blob/master/fr_47.jpg?raw=true "Pose 4")

- **Sample Convolutional Pose Machines**:
  ![Sample CPM](https://github.com/rockchik/Research-Project/blob/master/sample_cpm.png?raw=true "Sample CPM")

## Conclusion

Our proposed pipeline does not generalize well across the given data. Keypoint estimation techniques performed as expected, though failures in hand detection led to inaccuracies in keypoint estimation. Performance can be improved with more controlled data.

## Discussion

Deep Learning techniques have shown potential but often perform well on specific datasets. Traditional Computer Vision algorithms sometimes provide better results. The knot-tying process, with its inherent occlusions, poses challenges for accurate evaluation.

## Limitations

- **Complex Hand Shapes**: Knot-tying involves complex hand shapes that create significant occlusions.
- **System Complexity**: Developing an end-to-end integrated system remains challenging.
- **Algorithm Disparities**: Object detection and keypoint estimation algorithms have shown disparities in performance.

## Future Work

### Keypoints

- Focus on specific keypoints (index finger and thumb) rather than all hand joints.
- Incorporate depth images for improved accuracy in keypoint estimation.

### Bounding Boxes

- Improve bounding box detection accuracy by creating high-quality annotations.

### Data

- Develop a high-quality dataset collected in a controlled environment with expert surgeons.
- Test multiple camera angles for better keypoint estimation.

### Analysis

- Integrate traditional methods like Optical Flow with keypoint estimation.
- Explore matching correspondences in video for gesture analysis.
