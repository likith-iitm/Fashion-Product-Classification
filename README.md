# Fashion Product Classification using ResNet50

## Project Overview

This project develops a deep learning-based Fashion Product Classification system using Transfer Learning and Fine-Tuning with ResNet50.

The model classifies fashion product images into 54 categories such as Tshirts, Shirts, Watches, Handbags, Sandals, Sports Shoes, Kurtas, and more.

The project demonstrates an end-to-end computer vision pipeline including data preprocessing, exploratory data analysis, transfer learning, fine-tuning, model evaluation, and image inference.

---

## Dataset

Fashion Product Images Dataset

- Total Records: 44,424
- Images Used: 42,150
- Categories Used: 54
- Train Images: 30,348
- Validation Images: 3,372
- Test Images: 8,430

Dataset Source:
https://www.kaggle.com/datasets/paramaggarwal/fashion-product-images-dataset

---

## Project Pipeline

### Data Cleaning
- Removed categories with fewer than 100 samples
- Removed records with missing images
- Handled missing values

### Exploratory Data Analysis
- Category distribution analysis
- Gender distribution analysis
- Class imbalance analysis
- Image inspection

### Data Preprocessing
- Image resizing to 224 × 224
- Tensor conversion
- Normalization
- Label encoding

### Transfer Learning
- Loaded pretrained ResNet50 weights
- Frozen backbone layers
- Trained custom classification head

### Fine-Tuning
- Unfroze Layer4 of ResNet50
- Fine-tuned high-level image features
- Reduced learning rate for stable training

### Evaluation
- Validation Accuracy
- Test Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Top-5 Predictions

---

## Model Architecture

ResNet50 (Pretrained on ImageNet)

Stage 1:
- Feature Extraction
- Train only final classification layer

Stage 2:
- Fine-Tuning
- Unfreeze Layer4 and classifier

---

## Results

### Transfer Learning

Validation Accuracy: 83.69%

### Fine-Tuning

Validation Accuracy: 88.58%

### Final Test Performance

- Test Accuracy: 87.41%
- Weighted F1 Score: 0.87
- Macro F1 Score: 0.83

---

## Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- PIL

---

## Future Improvements

- EfficientNet implementation
- Visual Product Search
- Streamlit deployment
- Advanced data augmentation
- Model quantization

---

## Author

Likith Kota
