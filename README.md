# Hand Gesture Recognition Datasets
## Paper URL: None

## Description

We provide three different datasets for seven gestures performed each on 10 times by 5 volunteers, concluding in 50 samples for each gesture. The datasets are the following:
- Original dataset: contains the x and y coordinates, in addition to the depth value of the palm center, for each feature position.
- Motion-based normalized dataset: considering the motion of the hand instead of the raw coordinates.
- Frame sequence compressed dataset: considering the summation of a sequence of 30 frames as one single input (using the motion-based normalized dataset). 

Therefore, each dataset contains 350 gesture samples with the following gestures:
- Zoom in: two hands moving away horizontally
- Zoom out: two hands getting close to one another horizontally
- Move left: single hand moving left
- Move right: single hand moving right
- Move down: single hand moving down
- Move up: single hand moving up
- Press: single hand moving close to camera

A gesture consists of a sequence of consecutive frames. In this project, in order to create the dataset, we extract features from each frame and store them in a Comma Separated Value (CSV) file. The features are based on fingertip positions, hand palm centroid and its depth value. The created CSV file contains the following information for each row and gesture frame:
- Left centroid position (LC)
- Left fingers positions numbered clockwise (LF1, LF2, LF3, LF4, LF5)
- Left centroid depth (LCD)
- Right centroid position (RC)
- Right fingers positions numbered clockwise (RF1, RF2, RF3, RF4, RF5)
- Right centroid depth (RCD)
- Frame number (FN)
- Gesture number (GN)

One dataset row would be: LC, LF1, LF2, LF3, LF4, LF5, LCD, RC, RF1, RF2, RF3, RF4, RF5, RCD, FN, GN. Where each position is two dimensional (x and y coordinates). 

Regarding single hand gestures, we always store values on the left hand section in the CSV file and set the right hand section to zero. 
