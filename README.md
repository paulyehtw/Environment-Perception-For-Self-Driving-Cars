## Introduction
This is an assignment from [Visual Perception for Self-Driving Cars](https://www.coursera.org/learn/visual-perception-self-driving-cars) course of [Self-Driving Cars Specialization](https://www.coursera.org/specializations/self-driving-cars?) on Coursera.org.

In this assignment, you will:

1. Use the output of semantic segmentation neural networks to implement drivable space estimation in 3D.
2. Use the output of semantic segmentation neural networks to implement lane estimation.
3. Use the output of semantic segmentation to filter errors in the output of 2D object detectors.
4. Use the filtered 2D object detection results to determine how far obstacles are from the self-driving car.

## Prerequisites
**numpy** and **opencv** for python are installed.

## Implemented functions
### Drivable Space Estimation Using Semantic Segmentation Output
1. `xy_from_depth` : Estimating the x, y, and z coordinates of every pixel in the image
2. `ransac_plane_fit` : Estimating The Ground Plane Using RANSAC


<p align="center">
  <b>Freespace output:</b><br>
  <img  src="https://github.com/paulyehtw/Environment-Perception-For-Self-Driving-Cars/blob/master/images/occ_grid.png" height="47%" width="47%">
</p>

### Lane Estimation Using The Semantic Segmentation Output
1. `estimate_lane_lines` : Estimating Lane Boundary Proposals
2. `merge_lane_lines` : Merging and Filtering Lane Lines
<p align="center">
  <b>Lane detection output:</b><br>
  <img  src="https://github.com/paulyehtw/Environment-Perception-For-Self-Driving-Cars/blob/master/images/lanes_final.png" height="47%" width="47%">
</p>

### Computing Minimum Distance To Impact Using The Output of 2D Object Detection
1. `filter_detections_by_segmentation` : Filtering Out Unreliable Detections
2. `find_min_distance_to_detection` : Estimating Minimum Distance To Impact
<p align="center">
  <b>Bounding box and distance output:</b><br>
  <img  src="https://github.com/paulyehtw/Environment-Perception-For-Self-Driving-Cars/blob/master/images/distance_to_impace.png">
</p>

Check out more details in [Environment Perception For Self-Driving Cars - Learner - v1.ipynb](https://github.com/paulyehtw/Environment-Perception-For-Self-Driving-Cars/blob/master/Environment%20Perception%20For%20Self-Driving%20Cars%20-%20Learner%20-%20v1.ipynb)
