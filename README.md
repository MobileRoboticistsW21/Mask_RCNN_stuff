# Mask_RCNN_with_flow

## Run in Google Colab with our datset
Follow the instruction in the [Mask_RCNN_And_Optical_Flow.ipynb](https://colab.research.google.com/drive/12HZIfiC6xag7QCkzP16-bCUAVsX8DyIH?usp=sharing) in this [folder](https://drive.google.com/drive/folders/1q23QGS28uWzC22kCXXYILY4DEgrw3AjD?usp=sharing).

## Run with your own data
Download the Mask_RCNN_And_Optical_Flow.ipynb, change the path to your own data, and create folders to store intermidate data. Then follow the cells to produce a .JSON file containing Mask RCNN bounding boxes and optical flows. 

**This step should be run BEFORE performing GM-PHD filter, as it provides the input for the filter.**
