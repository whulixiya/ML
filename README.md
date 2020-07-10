# Superpixel-enhanced Deep Neural Forest for Remote Sensing Image Semantic Segmentation
Code for Paper 
[Superpixel-enhanced Deep Neural Forest for Remote Sensing Image Semantic Segmentation](https://www.sciencedirect.com/science/article/pii/S0924271619302606)
!['Can't load IMAGE'](https://github.com/whulixiya/ML/blob/master/mlPIPIP.png) 
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
## Evaluation
``` python
import predict_potsdam
predict_potsdam.process()

import predict_vaihingen
predict_vaihingen.process()
``` 
* The results include the predict RGB image, the predict Label image and the results.txt for accuracy.
* The whole evaluation process is about 20min.

## Results
<table>
	<tr>
		<td></td>
		<td>Imp.S.</td>
		<td></td>
		<td>Build.</td>
		<td></td>
		<td>Low.V.</td>
		<td></td>
		<td>Tree</td>
		<td></td>
		<td>Car</td>
		<td></td>
		<td>Mean</td>
		<td></td>
		<td>OA</td>
	</tr>
	<tr>
		<td></td>
		<td>F1</td>
		<td>IoU</td>
		<td>F1</td>
		<td>IoU</td>
		<td>F1</td>
		<td>IoU</td>
		<td>F1</td>
		<td>IoU</td>
		<td>F1</td>
		<td>IoU</td>
		<td>F1</td>
		<td>IoU</td>
		<td></td>
	</tr>
	<tr>
		<td>Pre-trained Model(P)</td>
		<td>93.6</td>
		<td>87.7</td>
		<td>96.3</td>
		<td>93</td>
		<td>89.8</td>
		<td>81.5</td>
		<td>92.7</td>
		<td>86.4</td>
		<td>96.7</td>
		<td>93.6</td>
		<td>93.8</td>
		<td>88.4</td>
		<td>92.1</td>
	</tr>
	<tr>
		<td>Paper(P)</td>
		<td>94.1</td>
		<td>88.9</td>
		<td>97.8</td>
		<td>95.7</td>
		<td>89.5</td>
		<td>80.9</td>
		<td>90.4</td>
		<td>82.5</td>
		<td>95.1</td>
		<td>90.7</td>
		<td>93.4</td>
		<td>87.7</td>
		<td>92.6</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td>Pre-trained Model(V)</td>
		<td>93.6</td>
		<td>87.9</td>
		<td>96.2</td>
		<td>92.6</td>
		<td>87.3</td>
		<td>77.4</td>
		<td>92.1</td>
		<td>85.3</td>
		<td>85.3</td>
		<td>74.4</td>
		<td>90.9</td>
		<td>83.5</td>
		<td>92.3</td>
	</tr>
	<tr>
		<td>Paper(V)</td>
		<td>93.4</td>
		<td>87.7</td>
		<td>97.6</td>
		<td>95.3</td>
		<td>87.4</td>
		<td>77.7</td>
		<td>91.2</td>
		<td>83.8</td>
		<td>85.2</td>
		<td>74.3</td>
		<td>91</td>
		<td>83.3</td>
		<td>92.2</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>
	<tr>
		<td></td>
	</tr>
</table>
