# Eye feature Segementation
## Introduction
The goal of this project is to segment the iris, pupil and sclera from an eye image. The iris is approximated as a circle, although the eyelid could cover it.  
In this project the iris, pupil and sclera can be segemented successfully, but parameter tuning (for thresholding, edge detection, ect.) must be optimized manually for each scenario. Also the segmentation modelused, requires some input pixel to distinguish the area to segment, which depends on the kind of image.  

After cloning this repository follow these steps:

## Dataset download (optional)
The dataset OpenEDS2020 offers eye images with the corresponding segmentation. You can store your own eye image in the folder images or download the OpenEDS2020 dataset.  
For future work, one can fine tune a segmentation model for this task.

## Segment Anything
Download the lightweighht version of segement anything (SAM) and store it in the folder models. For this project the model sam_vit_b_01ec64.pth was used, however you can use larger models if you like.  

## Virtual environement
Create your own virtual environment and install the required packages.  
```pip install requirements.txt```

## Evaluation 
Run the notebook **evaluation_nb.ipynb** to segement relevant parts in the image and output relevant metrics such as the Intersection over Union, the dice coefficient and the accuracy. 

## Conclusion
This project shows how to segement different eye features. However, its parameters are higly dependent on the input image, therefore parameter tuning is required for each image.  
For future work, one could use SAM to detect the iris and pupil as well, or find optimal paramters with grid search.
