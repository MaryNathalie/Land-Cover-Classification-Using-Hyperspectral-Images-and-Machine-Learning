# Land Cover Classification Using Hyperspectral Images and Machine Learning

### 🔍 Overview
This project provides a pipeline for classifying land cover using hyperspectral images (HSI) and machine learning techniques. Hyperspectral imaging captures data across multiple spectral bands, offering rich information that enables precise classification of different land cover types. By leveraging machine learning, this project aims to improve classification accuracy, and automate land cover analysis.

🔗 [Research Paper](https://github.com/MaryNathalie/Land-Cover-Classification-Using-Hyperspectral-Images-and-Machine-Learning/blob/main/documents/written_report.pdf) | [Presentation](https://github.com/MaryNathalie/Land-Cover-Classification-Using-Hyperspectral-Images-and-Machine-Learning/blob/main/documents/presentation_material.pdf)

### 🎯 Objectives
- Develop a robust workflow for preprocessing hyperspectral images
- Extract meaningful spectral and spatial features from HSI data
- Implement and compare multiple machine learning models for classification
- Evaluate model performance using standard classification metrics

### 🏭 Data Sources
The hyperspectral image data used in this project comes from [Grupo de Inteligencia Computacional](https://www.ehu.eus/ccwintco/index.php?title=Hyperspectral_Remote_Sensing_Scenes).

<p align="center">
<img src="https://github.com/MaryNathalie/Dengue-Forecasting-in-Philippine-Locations-Through-Climate-Based-Predictive-Models/blob/main/images/graphical_abstract.jpg" width=50% height=50%>
</p> 

#### 1. Indian Pines Hyperspectral Image
- Sensor: Airborne Visible Infrared Imaging Spectrometer (AVIRIS)
- Location: Indian Pines test site in North-Western Indiana, USA.
- It has 200 bands with a spatial resolution of 20-meter pixels and a spatial extent of 145 pixels by 145 pixels per band.
- It consists of the following land cover classes and their respective sample counts:

<div align="center">
  
| Class ID | Class Name                   | Sample Count |
|----------|------------------------------|--------------|
| 1        | Alfalfa                      | 46           |
| 2        | Corn Notill                   | 1,428        |
| 3        | Corn Mintill                  | 830          |
| 4        | Corn                          | 237          |
| 5        | Grass Pasture                 | 483          |
| 6        | Grass Trees                   | 730          |
| 7        | Grass Pasture Mowed           | 28           |
| 8        | Hay Windrowed                 | 478          |
| 9        | Oats                          | 20           |
| 10       | Soybean Notill                | 972          |
| 11       | Soybean Mintill               | 2,455        |
| 12       | Soybean Clean                 | 593          |
| 13       | Wheat                         | 205          |
| 14       | Woods                         | 1,265        |
| 15       | Building Grass Trees Drives   | 386          |
| 16       | Stone Steel Towers            | 93           |

</div>

<p align="center">
<img src="https://github.com/MaryNathalie/Dengue-Forecasting-in-Philippine-Locations-Through-Climate-Based-Predictive-Models/blob/main/images/graphical_abstract.jpg" width=50% height=50%>
</p> 
#### 2. Salinas Hyperspectral Image
- Airborne Visible Infrared Imaging Spectrometer (AVIRIS)
- Indian Pines test site in North-Western Indiana, USA.
- It has 200 bands with a spatial resolution of 20-meter pixels and a spatial extent of 145 pixels by 145 pixels per band.
- It consists of the following land cover classes and their respective sample counts:

<div align="center">

| Class ID | Class Name                      | Sample Count |
|----------|---------------------------------|--------------|
| 1        | Broccoli Green Weeds 1         | 2,009        |
| 2        | Broccoli Green Weeds 2         | 3,726        |
| 3        | Fallow                         | 1,976        |
| 4        | Fallow Rough Plough            | 1,394        |
| 5        | Fallow Smooth                  | 2,678        |
| 6        | Stubble                        | 3,959        |
| 7        | Celery                         | 3,579        |
| 8        | Grapes Untrained               | 11,271       |
| 9        | Soil Vineyard Develop          | 6,203        |
| 10       | Corn Senesced Green Weeds      | 3,278        |
| 11       | Lettuce Romaine 4 wk           | 1,068        |
| 12       | Lettuce Romaine 5 wk           | 1,927        |
| 13       | Lettuce Romaine 6 wk           | 916          |
| 14       | Lettuce Romaine 7 wk           | 1,070        |
| 15       | Vineyard Untrained             | 7,268        |
| 16       | Vineyard Vertical Trellis      | 1,807        |

</div>

### 🏗 Methodology

<p align="center">
<img src="https://github.com/MaryNathalie/Dengue-Forecasting-in-Philippine-Locations-Through-Climate-Based-Predictive-Models/blob/main/images/graphical_abstract.jpg" width=50% height=50%>
</p> 

#### 1. Preliminary Processing
- Standard Normalization, achieving zero mean and unit variance
- Principal Component Analysis, retaining a minimum of 99.9% image variance 
  - Indian Pines: 200 bands reduced to 108 bands
  - Salinas: 204 bands reduced to 19 bands
- 3D image cube transformed to a 2D structured format

#### 2. Modelling 
- **Machine Learning Models:**  (Tunes with GridSearchCV) SGD Regressor, XGBoost.
- Cross-Validation

### 📊 Results

### 📜 Future Work
#### 1. Sensitivity of Outbreak Thresholds
