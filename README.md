# Mask_RCNN_with_flow

## Run in Google Colab with our datset
Follow the instruction in the [Mask_RCNN_And_Optical_Flow.ipynb](https://colab.research.google.com/drive/12HZIfiC6xag7QCkzP16-bCUAVsX8DyIH?usp=sharing) in this [folder](https://drive.google.com/drive/folders/1q23QGS28uWzC22kCXXYILY4DEgrw3AjD?usp=sharing).

## Run with your own data
Note that for this repo the MASKRCNN directories and files were modified to run on google colab.

```
git clone https://github.com/MobileRoboticistsW21/Mask_RCNN_with_Optical_Flow.git
```

Within the [Mask_RCNN_And_Optical_Flow.ipynb](https://github.com/MobileRoboticistsW21/Mask_RCNN_with_Optical_Flow/blob/main/Mask_RCNN_And_Optical_Flow.ipynb), change the path to your own data, and create folders to store intermidate data. Then follow the cells to produce a .JSON file containing Mask RCNN bounding boxes and optical flows. 

Note that depending on google colab setting might need to change the amount of frames that run before getting saved into  pickle files to prevent RAM from crashing.

Would need to change these two lines
```
if (i - 49) % 50 == 0 or i == (len(file_names) - 1):
```

```
curr_image_idx = i * 50 + curr_pickle_idx 
```

**This step should be run BEFORE performing GM-PHD filter, as it provides the input for the filter.**
