# Visual-DLP: Visual Data Exfiltration Detection System

**Project ID:** O25-LIS4042-1    
**Date:** November 2025

## Overview
**Visual-DLP** is a Deep Learning-based computer vision system designed to detect **"Visual Exfiltration"**—the act of physically photographing a computer screen with a mobile device to steal sensitive information.

Traditional digital firewalls and DLP (Data Loss Prevention) software cannot detect this "analog" attack vector. This project bridges that gap, providing an automated solution to enforce physical security controls required by standards like **ISO/IEC 27001**, particularly for high-security banking environments.

## Key Features
* **Real-Time Detection:** Identifies the specific intent of data capture via webcam feed.
* **Zero False Alarm Policy:** Optimized for 1.00 Precision to prevent disruption of legitimate employee workflows.
* **Robustness:** Resilient to lighting changes, occlusions, and background clutter.

## Methodology
The system utilizes a **Transfer Learning** approach:
1.  **Backbone:** MobileNetV2 (pre-trained on ImageNet) used as a frozen feature extractor.
2.  **Classifier:** Custom fully connected layers trained on our specialized dataset.
3.  **Ablation Study:** Benchmarked against custom Deep CNNs and manual filtering techniques, proving that Transfer Learning yields the highest AUC (0.92).

##  Dataset: "Visual-DLP-16K"
We constructed a large-scale, balanced dataset to train this model:
**Total Images:** ~16,100
**Classes:** 50% Safe (Benign usage) / 50% Threat (Active capture).
**Scenarios:** Includes various angles, lighting conditions, and "discreet" attack attempts.

Due to GitHub storage limits (>100MB), the full dataset is hosted externally.

[**DOWNLOAD DATASET HERE (Google Drive)**](https://drive.google.com/file/d/1Ty_MAHWL9v6D8yJXRHS-_cOzDI2o0JZU/view?usp=sharing)
