# ISIC 2024 Skin Cancer Detection - Deep Learning Project

## 🎯 Project Overview

**Competition:** ISIC 2024 - Skin Cancer Detection with 3D-TBP (Kaggle)  
**Task:** Binary classification of dermoscopic images (Benign vs Malignant melanoma)  
**Team:** Nairi Keeney, Vrushabh Mudda, Marta Falceto Font  
**Final Submission:** November 13, 2025

---

## 📊 Final Results

### 🏆 Kaggle Leaderboard Performance

| Metric | Public Score | Private Score |
|--------|--------------|---------------|
| **pAUC (Competition Metric)** | **0.07560** | **0.07308** |

### 🧠 Model Comparison

| Model | pAUC | Status |
|-------|------|--------|
| **InceptionV3** ⭐ | **0.07560** | Best Model (3× better than others) |
| EfficientNetV2-B0-PR | 0.02599 | Completed |
| ResNet50 | 0.02237 | Completed |
| EfficientNetV2-B0-ROC | 0.01576 | Completed |
| Ensemble (90% InceptionV3) | 0.07560 | No improvement |

---

## 📈 Dataset Statistics

- **Total Training Images:** 401,059 dermoscopic images
- **Test Set:** ~500,000 images (hidden)
- **Class Distribution:** Benign (99.9%) vs Malignant (0.1%)
- **Imbalance Ratio:** 1000:1
- **Source:** International Skin Imaging Collaboration (ISIC) 2015-2024
- **Geographic Coverage:** 9 institutions across 3 continents

---

## ✅ Completed Milestones

### Data Preprocessing
- [x] Loaded 401K+ images from HDF5 format
- [x] Implemented class imbalance handling (oversampling + class weighting)
- [x] Stratified 80/20 train-validation split
- [x] Data augmentation (rotation, flip, zoom, brightness)
- [x] Architecture-specific preprocessing (299×299 for InceptionV3, 224×224 for ResNet/EfficientNet)

### Model Development
- [x] EfficientNetV2-B0 baseline (pAUC: 0.02599)
- [x] ResNet50 training (pAUC: 0.02237)
- [x] InceptionV3 training ⭐ (pAUC: 0.07560 - **BEST**)
- [x] Vision Transformer exploration
- [x] Transfer learning with ImageNet pretrained weights
- [x] Training optimization (EarlyStopping, ReduceLROnPlateau, ModelCheckpoint)

### Model Interpretability
- [x] Grad-CAM implementation on InceptionV3
- [x] Visualization of model attention for malignant cases (>84% confidence)
- [x] Visualization of model attention for benign cases (<4% confidence)
- [x] Clinical validation (ABCDE melanoma criteria alignment)

### Ensemble & Optimization
- [x] Equal-weight ensemble tested (50/50 split → failed)
- [x] Optimized ensemble tested (90% InceptionV3 → no improvement)
- [x] Conclusion: Single InceptionV3 model optimal

---

## 🎨 Key Findings

### Why InceptionV3 Won
- **Multi-scale feature learning:** Inception modules capture lesion features at varying sizes
- **3× better performance** than ResNet50 and EfficientNet variants
- **Clinically relevant attention:** Grad-CAM shows focus on asymmetry, irregular borders, color variation (ABCDE criteria)

### Grad-CAM Interpretability Examples
- **Malignant (97.6% confidence):** Strong activation on irregular lesion centers
- **Benign (1.6% confidence):** Minimal activation across normal skin



