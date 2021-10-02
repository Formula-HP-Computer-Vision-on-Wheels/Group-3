# Group 3

Project developed during the participation on the one week summer course of Formula HP Computer Vision on Wheels offered by the BEST UPC association.

## Goals

The goals for this project were to learn and use Agile methodology, learn how to efficiently work in a remotely workspace environment for group work and complete the proposed tasks by the professors.

## Tasks
&nbsp;1. Compute the Optical Flow to determine the direction of the vehicles.

- Detect the cars in the static camera videos by doing the average of the video frames to obtain the background. Then substract each frame minus the background image to obtain the moving objects.  
- Find the optical flow vectors of these moving objects.
- Determine the direction using the vectors.

&nbsp;2. For the in-car videos, detect if the car is changing lane.
- Do it by averaging the x-component of the motion vectors for all the frames.

### Optical flow task
#### Detection of the moving objects

The detection of the moving objects consists on the following steps:
- Average pixel in frames to retrieve the background.
- Generate ROI mask to scope our detection area.
- Perform erosion and dilatation to reduce noise.
- Substract the frames with the background to detect the moving objects.

#### Calculation of the optical flow

The calculation of the optical flow is done by obtaining the points of interest, and then tracking the motion of these points. The tracking of the points can be done by using Lucas-Kanade or by calculating their vectors.

### Lane-change dectection
The lane-change detection consists on the following steps:
- Generate ROI to scope the background.
- Use Farneback to detect the motion among all pixels.
- Check the x-component motion vector plot to derive conclusions.


