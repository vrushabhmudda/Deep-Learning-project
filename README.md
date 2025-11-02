# Deep-Learning-project
## 📈 Week 1 Progress (Oct 25 - 31)

### ✅ Completed

- [x] Dataset downloaded (2.7 GB) and organized
- [x] Exploratory Data Analysis (EDA) complete
- [x] Class distribution analyzed
- [x] Preprocessing pipeline implemented (224×224 resize, ImageNet normalization, augmentation)
- [x] Train/Val/Test split (80/10/10 stratified)
- [x] Evaluation metrics implemented (Accuracy, F1, AUC, Confusion Matrix)
- [x] Baseline models established (Random Guess, Majority Class)
- [x] First transfer learning model in training (EfficientNetB0)

### 📊 Week 1 Metrics

| Baseline | Accuracy | AUC | Status |
|----------|----------|-----|--------|
| Random Guess | 12.5% | 0.50 | ✅ |
| Majority Class | 40% | 0.50 | ✅ |

### 🧠 Data Overview

- **Total Images**: ~25,000
- **Classes**: 8 lesion types
- **Majority Class**: Nevus (~40%)
- **Target Minority**: Melanoma (~25%)

### 🔄 Week 2 Tasks (Nov 1-7)

- [ ] Train ResNet50 model
- [ ] Train InceptionV3 model
- [ ] Compare all 3 architectures (AUC ≥ 0.85)
- [ ] Fine-tune top 2 models
- [ ] Implement Grad-CAM visualizations
- [ ] Create ensemble model
