# 🧠 UNet with ResNet34 Backbone for Wrinkle Segmentation

This repository contains a high-performance semantic segmentation pipeline using a **U-Net architecture** with a **ResNet34 encoder**, specifically trained to identify **facial wrinkles** in high-resolution images. The model achieves **≈98% pixel-level accuracy**, demonstrating state-of-the-art performance in wrinkle detection for cosmetic and dermatological applications.

## 🚀 Highlights

- ⚙️ **Model Architecture**: U-Net with ResNet34 encoder from [segmentation_models.pytorch](https://github.com/qubvel/segmentation_models.pytorch)
- 🎯 **High Accuracy**: Achieves ≈98% pixel-wise accuracy on the validation dataset
- 🎨 **Visual Overlay**: Predicted wrinkle masks are blended over input images
- 💡 **Lightweight Inference**: Optimized for inference on both CPU and GPU (CUDA-compatible)
- 🤖 **Deep Learning Framework**: Built using PyTorch
- 🌍 **Live Demo**: [Try it on Hugging Face Spaces](https://huggingface.co/spaces/YOUR_USERNAME/wrinkle-segmentation-demo)
- 📈 **Training Done on**: Google Colab Pro+ with Tesla T4 GPU

---

## 🧬 Dataset

We used a curated dataset of facial images with manually annotated wrinkle regions.

- 📂 **Download Dataset**: [Wrinkle Segmentation Dataset](https://example.com/dataset-link) *(placeholder, replace with actual dataset URL)*

Each image includes:
- RGB facial images
- Binary mask annotations indicating wrinkle regions

---

## 🧠 Model Overview

The model uses the encoder-decoder design:

- **Encoder**: Pretrained ResNet34 backbone extracts hierarchical features
- **Decoder**: Symmetric upsampling layers reconstruct segmentation maps
- **Activation**: Sigmoid + Binary Thresholding at inference

**Loss Function**: BCE + Dice Loss  
**Optimizer**: Adam  
**Learning Rate**: 1e-4  
**Epochs**: 50  
**Augmentation**: Horizontal Flip, Random Crop, CLAHE

---

## 📊 Training Performance

<img src="https://raw.githubusercontent.com/YOUR_USERNAME/wrinkle-segmentation/main/assets/training_plot.png" width="600"/>

---

## 🖼️ Example Inference Output

### Input Image → Predicted Mask → Overlay

<p float="left">
  <img src="assets/padded_image.jpg" width="250"/>
  <img src="assets/pred_mask.jpg" width="250"/>
  <img src="assets/overlay_output.jpg" width="250"/>
</p>

---

## 🧪 Try It Yourself

**Google Colab Inference Notebook**:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/wrinkle-segmentation/blob/main/inference.ipynb)

---

## 🧰 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/wrinkle-segmentation.git
   cd wrinkle-segmentation
