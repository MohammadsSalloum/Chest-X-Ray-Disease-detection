# Chest X-ray Disease Detection

## 🧠 Project Goal
This project aims to build a deep learning model that classifies chest X-ray images as either **NORMAL** or **PNEUMONIA**. The model demonstrates how AI can support medical diagnosis by assisting in detecting pneumonia from X-ray images.

---

## 📦 Dataset
- Source: [Kaggle - Chest X-Ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- Total images: 5,863
- Classes: `NORMAL`, `PNEUMONIA`
- Dataset split:
  - **Train**: 5,216 images  
  - **Validation**: 16 images  
  - **Test**: 624 images  

> Note: The dataset is imbalanced, with more PNEUMONIA images than NORMAL.

---

## 🛠️ Project Steps

### 1. Data Exploration
- Visualized sample X-ray images from both classes.
- Checked class distribution for imbalances.

### 2. Data Preprocessing
- Resized images to 150x150 pixels.
- Converted images to **grayscale** to simplify processing.
- Normalized pixel values (0-1 range).

### 3. Model Building
- CNN built from scratch:
  - Multiple Conv2D + MaxPooling layers
  - Dense layers at the end
- Compiled with:
  - Loss: Binary Crossentropy
  - Optimizer: Adam
  - Metrics: Accuracy, Precision, Recall, AUC

### 4. Evaluation
- Evaluated on the test set:
  - Test Loss: 0.5682  
  - Test Accuracy: 0.7468  
  - Precision: 0.9640  
  - Recall: 0.6179  
  - AUC: 0.9214
- Confusion matrix and classification report generated.
- Visualized some sample predictions.

---

## 📊 Results
| Class       | Precision | Recall | F1-score | Support |
|------------|-----------|--------|----------|---------|
| NORMAL     | 0.60      | 0.96   | 0.74     | 234     |
| PNEUMONIA  | 0.96      | 0.62   | 0.75     | 390     |
| **Accuracy** |           |        | 0.75     | 624     |

> The model is very precise when predicting PNEUMONIA, but it misses some true pneumonia cases (moderate recall).  

