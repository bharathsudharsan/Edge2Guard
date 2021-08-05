# Edge2Guard: Botnet Attacks Detection on IoT Devices

## Overview

Edge2Guard (E2G) enables IoT devices to instantly detect attacks without depending on networks (standalone) or any external protection mechanisms. Due to the resource-friendly design of E2G models, they can execute on MCU-based tiny devices, without imposing computational pressure, also without disturbing device routine.

Link to paper: [https://ieeexplore.ieee.org/document/9431086](https://ieeexplore.ieee.org/document/9431086)

## Data Profiling

**Benign/Gafgyt/Mirai_data_profile.html:** Here, we generate and present the profile reports from the DataFrame of the Benign/Gafgyt/Mirai traffic data to facilitate exploratory data analysis. In the report's *Overview* section, the high-level data statistics starting from the number of variables until the average record size in memory is available. The next variables section contains multiple subsections such as *Statistics, Histograms, Common values*, and *Extreme values* to describe each of the available 117 variables.

**Note:** Download the Benign/Gafgyt/Mirai_data_profile.html file, then open via browser (cannot view directly from the repo). The file content sample is shown in below image (scroll after opening .html files to explore more).
 
![alt text](https://github.com/bharathsudharsan/Edge2Guard/blob/main/Mirai_report_html_file.PNG)

## Data Preprocessing, Analysis and Model Training

**Dataset_wrangling.ipynb:** Loads the N-BaIoT dataset and presents information such as the data dimension, individual device data count and feature information, memory consumed by each class of data with its range index, and data profile of each malware. It also checks for any null values and combines all data into one CSV file. 

**Exploratory_data_analysis.ipynb:** Here, we used the PCA dimensionality reduction method to mathematically reduce the 115 features into 2 features and visualize them by making 2D and 3D scatter plots, using which we explore the patterns and find out trends between the malicious and benign traffic data.
 
**Data_preprocessing_and_E2G_model_training.ipynb:** We pre-process the data to group it into four categories. We follow a 70-30 Training-testing split and used all the 115 features. We use this pre-processed data and train multiple supervised learning and One-class learning models, and evaluate it using Accuracy, F1 score, Kappa, and Matthews Correlation Coefficient (MCC) metrics.

## Evaluation Results of Models

**E2G_model_training_and_evaluation_results.docx:** This file contains the detailed evaluation results (confusion Matrix, precision, recall, F1-score, support, accuracy, macro avg, weighted avg) of all the types of E2G attack detecting classifiers trained using the preprocessed data along with the feature importance for each type of model. 

The results are breifly presented in below Tables.

![alt text](https://github.com/bharathsudharsan/Edge2Guard/blob/main/Model_perf_comparison.PNG)

![alt text](https://github.com/bharathsudharsan/Edge2Guard/blob/main/Top_perform_models.PNG)

**If the code is useful, please consider citing Edge2Guard paper using the BibTex entry below.**

```
@inproceedings{sudharsan2021edge2guard,
  title={Edge2Guard: Botnet Attacks Detecting Offline Models for Resource-Constrained IoT Devices},
  author={Sudharsan, Bharath and Sundaram, Dineshkumar and Patel, Pankesh and Breslin, John G and Ali, Muhammad Intizar},
  booktitle={2021 IEEE International Conference on Pervasive Computing and Communications Workshops and other Affiliated Events (PerCom Workshops)},
  pages={680--685},
  year={2021},
  organization={IEEE}
}
```
For any clarification/further information please don't hesitate to contact me. Email: b.sudharsan1@nuigalway.ie