# Superpixel-enhanced Deep Neural Forest for Remote Sensing Image Semantic Segmentation
Code for Paper 
![Superpixel-enhanced Deep Neural Forest for Remote Sensing Image Semantic Segmentation](https://github.com/whulixiya/ML/blob/master/mlPIPIP.png)

## Environments
* Python 3.6.2
* Tensorflow 1.6.0
* Numpy 1.13.1
* opencv-python
* Matplotlib
* scipy

## Data
*	Download the test image (RGB for Potsdam/IRRG for Vaihingen) and RGB label image (Fully Reference/No Boundary) from ISPRS 2D semantic labelling website.
*	Transfer the RGB label image to the corresponding label image (provided).
|         |       | Table 1 Label  Transferring |      |      |
| ------- | ----- | --------------------------- | ---- | ---- |
|         | Index | R                           | G    | B    |
| Imp     | 0     | 255                         | 255  | 255  |
| Build   | 1     | 0                           | 0    | 255  |
| Low     | 2     | 0                           | 255  | 255  |
| Tree    | 3     | 0                           | 255  | 0    |
| Car     | 4     | 255                         | 255  | 0    |
| Cluster | 5     | 255                         | 0    | 0    |
| Un      | 6     | 0                           | 0    | 0    |
*	Rename the testing image and label image.
