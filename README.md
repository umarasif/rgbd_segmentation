# RGBD Segmentation Software
This software performs segmentation of RGBD images (an RGB image and a registered depth image).

This software is built upon the following research work.

- U. Asif, M. Bennamoun and F. Sohel, Unsupervised Segmentation of Unknown Objects in Complex Environments, Autonomous Robots”, vol. 40, no. 5, pp. 805-829, 2016.
- U. Asif, M. Bennamoun and F. Sohel, A Model-free approach for the Segmentation of Unknown Objects, “IEEE International Conference on Intelligent Robotics and Systems (IROS)”, pp. 4914-4921, Chicago, September, 2014.
- U. Asif, M. Bennamoun and F. Sohel, Model-Free Segmentation and Grasp Selection of Unknown Stacked Objects, “European Conference on Computer Vision (ECCV)”, pp. 659-674, Zurich, September, 2014.

Note that this software is still work-in-progress. It is built upon unoptimized versions of the above algorithms without real-time performance. The default parameters are not optimal for every RGB-D image, and the output varies with respect to the parameters. If you use this software, please cite the above research.

## Requirements

This software was built and tested using Windows 7. The software has dependencies on the following libraries which are already included in the repository as dll files.

- Accord
- AForge
- EmguCV
- OpenCV
- OpenTK

## Operation
### Inputs
RGB image and a depth image with 640×480 resolution.
Note that the parameters of the software are tuned with respect to the default 640×480 image size.
### Outputs
1. initial segmentation: oversegmentation into structurally planar patches.
2. depth segmentation: perceptual grouping of patches into object hypotheses using only depth information.
3. rgbd segmentation: refinement of depth segmentation using both color and depth information.
## GUI based operation

1. Run the software from RGBD_segmentation.exe
2. Load an RGB image and a registered depth image using the GUI.
3. Click **Run** to perform segmentation.

The segmentation results can be saved as PNG files by clicking the **Save results** button on the GUI. Note that the default parameters are not optimal for every RGB-D image. The values can be changed using the sliders to obtain the best segmentation. Every time the parameters are changed, click **Run** to produce the new results.

## Command line based operation

### Parameters
| Parameter name                      | Default Value 	| Description                                                       	|
|------------------------------------	|----------------	|--------------------------------------------------------------------	|
| rgb_path      	                  | current application folder      | absolute path of an RGB image                      	|
| depth_path      	                | current application folder      | absolute path of a depth image                      	|
| output_path      	                | current application folder      | absolute path of output folder                      	|
| sp_flag      	                    | false      | enable/disable generation of superpixels                      	|
| bdry_thresh      	                  | 242      | intensity value (0-255) at which boundaries are detected in the RGBD image. A low value causes undersegmentation.                    	|
| depth_thresh      	                  | 4000      | depth values higher than this value wiuld be set to 0 in the depth image.                    	|
| smoothness||
|sp_size|200| Maximum size of a superpixel.
|convex_thresh| 10| A higher value causes undersegmentation.
|disp_flag|true|display the output segmentations.

## Examples
1. Generate superpixels:
rgbd_segmentation console sp_flag=true

2. Turn-off output visualization:
rgbd_segmentation console disp_flag=false

