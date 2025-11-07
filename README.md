# 🧠 Hybrid CNN + ViT Cancer Detection Diagnostic Tool with Grad-CAM Visualization 🔬

> **An AI-powered diagnostic tool for accurate and explainable cancer detection from histopathological images**

---

## 📖 Project Overview

This project presents an **AI-based diagnostic system** that uses a **Hybrid Deep Learning Model (CNN + Vision Transformer)** to automatically detect **cancerous tissues** from **histopathological images**.  
The system assists **pathologists and clinicians** by providing **accurate, fast, and explainable cancer diagnosis** through visual heatmaps and detailed reports.

The hybrid architecture combines **Convolutional Neural Networks (CNN)** for extracting local texture features and **Vision Transformers (ViT)** for capturing global contextual information.  
To improve interpretability, **Grad-CAM (Gradient-weighted Class Activation Mapping)** highlights tumor regions that influenced the model’s decision — making the AI system transparent and trustworthy in clinical settings.

---

## 🧩 Key Features

- 🧠 **AI Diagnostic Tool for Cancer Detection** — classifies tissue images as *Tumor* or *Normal*  
- ⚙️ **Hybrid CNN + ViT Model** — merges local and global image understanding  
- 🌈 **Grad-CAM Heatmaps** — visualize tumor regions for transparent AI decisions  
- 📊 **Performance Metrics** — includes ROC-AUC, PR Curve, Confusion Matrix, and accuracy plots  
- 🧾 **Auto-Generated Report** — includes confidence, uncertainty, tumor area %, and aggressiveness estimation  

---

## 🗂️ Dataset

- **Dataset Source:** [Kaggle – Histopathologic Cancer Detection](https://www.kaggle.com/competitions/histopathologic-cancer-detection)
- **Type:** Microscopic tissue images (patches of size 96×96)
- **Classes:**
  - `1` → Tumor (Cancerous)
  - `0` → Normal (Healthy)
- All images were resized to **224×224** before training and normalized.

---

## ⚙️ Model Architecture

| Component | Description |
|------------|-------------|
| **ResNet-18 (CNN)** | Extracts spatial and textural features from tissue images |
| **Vision Transformer (ViT)** | Captures global relationships between image regions |
| **Fusion Layer** | Concatenates CNN and ViT features |
| **Fully Connected Classifier** | Produces final Tumor / Normal output |
| **Softmax Layer** | Converts logits to class probabilities |

---

## 🧮 Training Configuration

| Parameter | Value |
|------------|--------|
| Batch Size | 64 |
| Epochs | 3 |
| Learning Rate | 1e-4 |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |
| Frameworks Used | PyTorch, TIMM, OpenCV, Pandas, Matplotlib |

---

## 📈 Model Evaluation

| Metric | Result |
|--------|---------|
| **Confusion Matrix** | [[2174, 198], [104, 1524]] |
| **Accuracy** | ≈ 95% |
| **ROC-AUC Score** | 0.977 |
| **Average Precision (AP)** | 0.972 |

These results demonstrate that the diagnostic tool achieves **high accuracy and robust predictive performance**, effectively distinguishing between cancerous and normal tissue patches.

---

## 🔥 Explainability (Grad-CAM)

**Grad-CAM** visualizations generate color-coded heatmaps that show **where the model focused** when predicting a tumor.  
This provides **explainability** — a crucial aspect in **medical AI**, allowing pathologists to verify if the model is focusing on actual cancerous regions rather than irrelevant patterns.

---

## 🧾 Inference Report

After running inference, a detailed **CSV report** is automatically generated, containing:
- Image ID  
- Predicted Label (Tumor / Normal)  
- Probability Scores  
- Confidence and Uncertainty  
- Tumor Area Percentage  
- Aggressiveness Level (High / Medium / Low)  
- Heatmap File Name  

---

## 📊 Result Visualizations

The following graphs and visual outputs are produced:
- 📉 **Training Loss over Epochs**
- 📈 **Training Accuracy over Epochs**
- 🔵 **Confusion Matrix Heatmap**
- 🟢 **ROC-AUC Curve**
- 🟣 **Precision-Recall Curve**
- 🔥 **Grad-CAM Heatmap Overlays**

---

## 🧠 Domain

- **Main Domain:** Artificial Intelligence (AI)  
- **Subdomain:** Computer Vision / Medical Image Analysis  
- **Application Area:** Cancer Detection & Diagnostic Imaging  

---

## 🚀 Future Enhancements

- Extend to **multi-cancer classification** (e.g., breast, lung, skin)
- Deploy as a **web-based diagnostic dashboard** (using Streamlit or Flask)
- Integrate **Explainable AI (XAI)** methods like SHAP or LIME
- Enable **real-time inference** for clinical use

---

## 👩‍💻 Author

**Minna Fathima**  
*M.Tech Integrated Software Engineering*  
VIT Chennai 
 
🔗 GitHub: [https://github.com/MinnaFathima](https://github.com/MinnaFathima)

---


## 🖼️ Sample Output

| Original Image | Grad-CAM Heatmap |
|----------------|------------------|
| ![Original](patho_outputs/sample_original.png) | ![Heatmap](patho_outputs/sample_heatmap.png) |

---

### ⭐ If you found this project useful, don’t forget to **Star ⭐ the repository!**
