# XAI in Biomedicine: TB and Pneumonia Detection from Chest X-rays

We show the potential for DL/CNN models for classification of tuberculosis (TB) from chest radiography images. We align with WHO's promotion of improving the accessibility, together with the quality, of diagnostic services. By using models built from scratch and XAI techniques, we try to understand how the model arrived at a particular diagnosis.

Follow the notebook to:
- Preprocess X-ray images (resizing, grayscale→RGB conversion).
- Train ResNet/DenseNet models with transfer learning.
- Evaluate performance using F1 score, precision, and recall.
- Generate XAI visualizations (Grad-CAM, SHAP, LIME).

![Deep Learning in Biomedicine](https://img.shields.io/badge/Field-Biomedical_AI-blue)
![License](https://img.shields.io/badge/License-MIT-green)

**Authors**: Alessia Lindemann, M. Olmo Nogara Notarianni, Sara Paratico  

## Overview
This repository contains code and a detailed report for a classification task for **tuberculosis (TB)** and **pneumonia** detection from chest X-ray images. The goal was to develop a model achieving an F1 score >75% using ResNet and DenseNet architectures, alongside using explainable AI (XAI) techniques to interpret predictions.
The dataset utilized in this study consisted of 15470 thoracic X-ray images in .png or .jpeg format, divided into three classes: normal (N), pneumonia (P) and tuberculosis (T) with 9354, 4250 and 1866 cases respectively. Unfortunately, the dataset is not available.

## Key Features
- **Models**: ResNet50V2, DenseNet121, and a custom CNN.
- **Techniques**: Transfer learning, data augmentation, hyperparameter tuning with Keras Tuner.
- **XAI Methods**: Grad-CAM, SHAP, LIME, and confidence score analysis.
- **Performance**: Achieved **F1 scores up to 0.97 for pneumonia** and **0.91 for TB** using DenseNet.


## Prerequisites
- Python 3.8+
- TensorFlow 2.x
- Libraries: NumPy, Pandas, Matplotlib, SHAP, Lime, Scikit-learn


## Results Summary
| Model       | TB F1-Score | Pneumonia F1-Score | Parameters |
|-------------|-------------|---------------------|------------|
| ResNet50V2  | 0.88        | 0.97                | 25.6M      |
| DenseNet121 | 0.91        | 0.97                | 6.9M       |

- **Best Performance**: DenseNet achieved higher F1 scores with fewer parameters.
- **Key Insight**: Adding dropout improved ResNet's TB precision by **9.8%**.

## Explainable AI (XAI)
- **Grad-CAM**: Highlighted lung regions critical for predictions.
- **SHAP/LIME**: Identified pixel-level contributions to diagnoses.
- **Confidence Scores**: Analyzed model certainty via Top-2 Differences.

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgments
- Pretrained models: ImageNet weights for ResNet/DenseNet.
- WHO guidelines for TB diagnosis.

## Contact
For questions, contact: [olmonotarianni@gmail.com](mailto:olmonotarianni@gmail.com).
```
