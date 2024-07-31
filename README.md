## INTRODUCTION
The rapid increase in the number of vehicles on roads has necessitated the development of effective solutions to mitigate traffic congestion. Automatic Vehicle Detection (AVD) systems have become crucial for real-time traffic observation and management, forming an integral part of Intelligent Transportation Systems (ITS) and smart city applications. The advent of self-driving cars and advanced driver assistance systems further emphasizes the need for precise and reliable AVD.
Despite advancements in AVD, there is significant room for improvement, especially under diverse weather and lighting conditions. Traditional vehicle detection systems often struggle with varying environmental factors, leading to decreased performance. Addressing these challenges is essential for enhancing the accuracy and reliability of AVD systems.
## Report
To get detailed information on the methodology and working of the model, view this [VDVWC_Report.pdf](https://github.com/user-attachments/files/16440708/VDVWC_Report.pdf)
## a) Dataset

This research introduces a novel vehicle detection system leveraging the JUVDv2-VDVWC dataset. This dataset is designed to benchmark vehicle detection performance under varied weather and lighting conditions, featuring 2,600 training images, and 200 validation images annotated in the YOLO format.

## b) Proposed Methodology
Our methodology employs a hybrid approach using two ResNet50 models for binary classification of images into day/night and rainy/sunny categories. Following this classification, four specialized YOLOv8x models, each trained on specific subsets of the dataset, perform object detection. An ensembling technique combines predictions from primary and secondary models, enhancing detection accuracy and reducing overfitting.

## c) Significance
This research aims to demonstrate that the proposed system significantly improves vehicle detection accuracy under diverse environmental conditions, contributing to more efficient and reliable ITS and smart city applications.

## Accuracy And Benchmarks

Weather_Prediction Resnet50 Model:

	Weighted Average Precision: 0.88
  
  	F1 score: 0.86

Daytime_Prediction Resnet50 Model:

  	Weighted Average Precision: 0.89
  
  	F1 score: 0.85

Vehicle detection YOLOv8x model:

  	mAP50: 0.75747
  
  	mAP50-95: 0.40131
