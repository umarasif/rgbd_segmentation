# 3D Segmentation Software
A GUI-based tool to segment RGB-D images.

This software is built upon the following research work.

0:    U. Asif, M. Bennamoun and F. Sohel, Unsupervised Segmentation of Unknown Objects in Complex Environments, Autonomous Robots”, vol. 40, no. 5, pp. 805-829, 2016.
1:    U. Asif, M. Bennamoun and F. Sohel, A Model-free approach for the Segmentation of Unknown Objects, “IEEE International Conference on Intelligent Robotics and Systems (IROS)”, pp. 4914-4921, Chicago, September, 2014.
2:    U. Asif, M. Bennamoun and F. Sohel, Model-Free Segmentation and Grasp Selection of Unknown Stacked Objects, “European Conference on Computer Vision (ECCV)”, pp. 659-674, Zurich, September, 2014.

Note that this software is still work-in-progress. It is built upon unoptimized versions of the above algorithms without real-time performance. The default parameters are not optimal for every RGB-D image, and the output varies with respect to the parameters. If you use this software, please cite the above research.
Requirements

This software was built and tested using Windows 7.

The software has dependencies on the following libraries which are already included in the repository as dll files.

    Accord
    AForge
    EmguCV
    OpenCV
    OpenTK

GUI based operation

    Run the software from RGBD_segmentation.exe
    Load an RGB image and a registered depth image using the GUI.
    Click Run to perform segmentation.
    The segmentation results can be saved as PNG files by clicking the Save results button on the GUI. Note that the default parameters are not optimal for every RGB-D image. The values can be changed using the sliders to obtain the best segmentation. Every time the parameters are changed, click Run to produce the new results.

Command line based operation
