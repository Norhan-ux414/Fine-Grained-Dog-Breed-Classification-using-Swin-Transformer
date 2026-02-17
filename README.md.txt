#  Dog Breed Classification using Swin Transformer (Fine-Tuning)

This project implements fine-tuning of a pre-trained Swin Transformer model for fine-grained dog breed classification using the Stanford Dogs dataset.

---

##  Dataset

- Dataset: Stanford Dogs
- 120 dog breeds
- ~20,580 images
- Stratified split: 80% Train / 10% Validation / 10% Test

---

##  Model

- Architecture: Swin-Tiny (patch4_window7_224)
- Pre-trained on ImageNet
- Fine-tuned by:
  - Replacing classification head (120 classes)
  - Unfreezing:
    - Classification head
    - Last Swin Transformer block

---

##  Training Strategy

- Optimizer: AdamW
- Learning Rate:
  - Head training: 1e-3
  - Fine-tuning: 1e-4
- Data augmentation:
  - RandomResizedCrop
  - Horizontal Flip
  - Color Jitter
- Image size: 224x224

---

## Results

### Validation Performance

- Accuracy ≈ 90%
- Macro F1 ≈ 0.90

### Test Performance

- Accuracy: **92.9%**
- Macro Avg F1: **0.9269**
- Weighted Avg F1: **0.9282**

The model generalizes well and performs strongly on fine-grained classification.

---

##  Real-Time Testing

Sample predictions were visualized on unseen test images, demonstrating accurate breed classification.

---

##  Handling Complex Scenarios

- Class imbalance was addressed using stratified splitting.
- Fine-tuning strategy helped improve generalization while avoiding overfitting.

---

##  How to Run

1. Install dependencies

2. Update dataset path

3. Run the notebook sequentially

---

##  Author

- Nourhan Yehia


