# 🚦 Traffic Sign Recognition with Data Augmentation  

A deep learning project for recognizing **German Traffic Signs (GTSRB)** using **Convolutional Neural Networks (CNNs)**.  
The model classifies traffic signs into **43 categories**, playing a crucial role in **autonomous driving** and **ADAS (Advanced Driver-Assistance Systems)**.  

---

## 📌 Overview  
- Built a robust CNN pipeline to classify traffic signs.  
- Applied **data augmentation** for better generalization.  
- Achieved **95–97% accuracy** on test data.  
- Evaluated with **accuracy, precision, recall, and F1-score**.  

---

## 🎯 Objectives  
- Train a CNN on the **GTSRB dataset**.  
- Improve performance with **augmentation techniques**.  
- Compare baseline vs augmented results.  
- Provide a reproducible pipeline for research & deployment.  

---

## 📂 Dataset  
- **Name:** German Traffic Sign Recognition Benchmark (GTSRB)  
- **Classes:** 43  
- **Training Images:** ~39,000  
- **Test Images:** ~12,000  
- **Image Size:** 32×32×3  

---

## 🔧 Methodology  

### 1️⃣ Data Preprocessing  
- Resize to `32×32×3`  
- Normalize to `[0,1]`  
- One-hot encode labels  

### 2️⃣ Data Augmentation  
- Random rotations (±20°)  
- Zoom (0.8–1.2×)  
- Shifts (±10%)  
- Brightness variation (±20%)  
- Shear + flips  

### 3️⃣ Model Architecture (CNN)  
- Conv2D → ReLU → Conv2D → ReLU → MaxPooling → Dropout  
- Conv2D → ReLU → MaxPooling → Dropout  
- Flatten → Dense → Dropout → Softmax (43 classes)  

---

## ⚙️ Training Setup  
- **Loss:** Categorical Crossentropy  
- **Optimizer:** Adam (lr=0.001)  
- **Batch Size:** 32 / 64  
- **Epochs:** 30–50  
- **Callbacks:** EarlyStopping & ModelCheckpoint  

---

## 📊 Results  

| Model                | Accuracy | Precision | Recall | F1-score |
|-----------------------|----------|-----------|--------|----------|
| Baseline CNN          | ~92%     | 90%       | 90%    | 90%      |
| With Augmentation     | 95–97%   | 94%       | 94%    | 94%      |

---

