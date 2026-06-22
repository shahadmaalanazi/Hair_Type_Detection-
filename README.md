# Hair Type Classification Using EfficientNet-B0

## Overview

Hair type classification plays an important role in personalized hair care and beauty-related applications. However, accurately distinguishing between different hair textures can be challenging due to variations in lighting, image quality, and natural hair appearance.

This project presents a deep learning-based hair type classification system using EfficientNet-B0 and transfer learning techniques. A pretrained EfficientNet-B0 model was fine-tuned on a labeled hair type dataset to automatically recognize and classify hair textures from images. The project includes data preprocessing, augmentation, model training, fine-tuning, and performance evaluation using standard classification metrics.

By leveraging transfer learning, the model is able to extract meaningful visual features while reducing training time and computational cost. The final system demonstrates the effectiveness of EfficientNet-B0 for image classification tasks and provides a foundation for future applications in hair analysis, beauty technology, and AI-powered recommendation systems.

## Features

- Transfer Learning using EfficientNet-B0
- Data Augmentation
- Early Stopping
- Fine-Tuning
- Performance Evaluation
- Confusion Matrix Visualization
- Sample Prediction Visualization

---

## Dataset

Dataset Source:

https://www.kaggle.com/datasets/kavyasreeb/hair-type-dataset

Dataset split:

- Training Set: 70%
- Test Set: 30%

---

## Data Preprocessing

The following preprocessing techniques were applied:

- Resize images to 224 × 224
- RGB conversion
- Image normalization
- Random Horizontal Flip
- Random Rotation
- Color Jitter

---

## Model

The model uses a pretrained EfficientNet-B0 backbone.

### Training Settings

| Parameter | Value |
|------------|--------|
| Batch Size | 16 |
| Optimizer | Adam |
| Initial Learning Rate | 5e-5 |
| Fine-Tuning Learning Rate | 1e-5 |
| Loss Function | CrossEntropyLoss |
| Epochs | 30 |
| Early Stopping Patience | 5 |

---

## Fine-Tuning

After the initial training phase:

- Best model weights are saved.
- Selected EfficientNet layers are unfrozen.
- Additional fine-tuning is performed with a lower learning rate.

---

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Libraries Used

```python
torch
torchvision
timm
datasets
transformers
numpy
pandas
matplotlib
scikit-learn
kagglehub
```

## Project Structure

```text
.
├── efficientnet_b0.py
├── best_model.pth
├── best_model_finetuned.pth
├── dataset/
└── README.md
```

## Workflow

```text
Dataset
   ↓
Preprocessing
   ↓
Data Augmentation
   ↓
Train/Test Split
   ↓
EfficientNet-B0
   ↓
Training
   ↓
Early Stopping
   ↓
Fine-Tuning
   ↓
Evaluation
```

## Results

The model successfully classifies hair types using transfer learning and fine-tuning techniques. Performance is evaluated using standard classification metrics and visual analysis tools.

## Kaggle
https://www.kaggle.com/code/shahad05/hair-detection-using-efficientnet-b0

## Author

Shahad Alanazi
Rana alashur
shaden 
zainab
