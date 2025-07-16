# A Comparative Study of ResNet Variants for Colon Cancer Histopathological Image Classification Using MTANv3 Attention

This repository contains the code and resources for the research paper titled **"A Comparative Study of ResNet Variants for Colon Cancer Histopathological Image Classification Using MTANv3 Attention"**. The study evaluates and compares three ResNet variants—**ResNet-18**, **ResNet-50 v1**, and **ResNet-50 v1.5 with MTANv3 attention**—on the LC25000 colon histopathological dataset.

---

## 📌 Abstract

Colon cancer remains one of the leading causes of cancer mortality. This study implements a comparative evaluation of deep convolutional neural networks integrated with attention mechanisms to enhance the diagnostic classification of histopathological images. Results indicate that ResNet-50 v1.5 + MTANv3 provides superior performance across key metrics.

---

## 🧠 Model Architectures

| Model Variant            | Description                                               |
|--------------------------|-----------------------------------------------------------|
| ResNet-18                | Lightweight model with fewer residual layers              |
| ResNet-50 v1             | Deep residual network (torchvision-based)                 |
| ResNet-50 v1.5 + MTANv3  | TIMM-based ResNet50d variant with MTANv3 attention module |

---

## 📂 Dataset

- **Source**: LC25000 (Colon histopathology subset)
- **Classes**:
  - `colon_n`: Normal colon tissue (2,500 images)
  - `colon_aca`: Adenocarcinoma colon tissue (2,500 images)
- **Preprocessing**:
  - Resize to 112×112
  - Horizontal flipping
  - ImageNet normalization

[LC25000 on Kaggle](https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images)

---

## ⚙️ Training Configuration

- **Loss Function**: Binary Cross-Entropy (BCEWithLogitsLoss)
- **Optimizer**: Adam
- **Learning Rate**: 1e-4
- **Epochs**: 10
- **Batch Size**: 32
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score

---

## 📈 Results Summary (Replace with actual values)

| Model                   | Accuracy (%) | Precision | Recall | F1-Score |
|------------------------|--------------|-----------|--------|----------|
| ResNet-18              | XX.XX        | XX.XX     | XX.XX  | XX.XX    |
| ResNet-50 v1           | YY.YY        | YY.YY     | YY.YY  | YY.YY    |
| ResNet-50 v1.5 + MTANv3| ZZ.ZZ        | ZZ.ZZ     | ZZ.ZZ  | ZZ.ZZ    |

> 📝 The MTANv3-enhanced ResNet-50 v1.5 consistently outperformed others.

---

## 🗂 Files in This Repository

- `train_resnet18.py` – Training with ResNet-18
- `train_resnet50.py` – Training with ResNet-50 v1
- `train_resnet50v15_mtanv3.py` – Training with ResNet-50 v1.5 + MTANv3
- `README.md` – Project documentation
- `ResNetV2_Colon_Report.docx` – Word report including results and visualizations
- `*.csv` – Accuracy/loss/confusion matrix outputs
- `*.png` – Plots of accuracy, loss, and confusion matrix
- `*.pth` – Saved PyTorch model weights

---

## 📦 Installation

```bash
pip install torch torchvision timm pandas seaborn scikit-learn matplotlib python-docx
