# 🔥 CelebA Image Super-Resolution with U-Net

**Turn tiny pixels into high-definition perfection.**

This project implements a **U-Net model for image super-resolution**, transforming low-resolution images (64x64) into crisp, high-resolution versions (512x512). Trained on the iconic **CelebA dataset**, the model leverages the encoder-decoder architecture of U-Net with skip connections to preserve both global structure and fine-grained details.

---

## 🎯 Project Goal

Super-resolution is the art of making images sharper, clearer, and more detailed. Here, we aim to:

* Take a **64x64 RGB image** as input.
* Generate a **512x512 RGB image** with improved visual fidelity.

---

## 🛠 Features

* **U-Net Architecture:** Classic encoder-decoder design with skip connections for feature retention.
* **Custom Upsampling:** Extra layers to upscale images from 64x64 → 512x512.
* **Real-Time Visualization:** Automatically saves and displays original, low-resolution, ground truth, and super-resolved images at the end of each epoch.
* **Flexible Training Pipeline:** Easy-to-use data generator for batch training on CelebA dataset.
* **Checkpointing:** Automatically saves model weights per epoch for safe recovery and experimentation.

---

## ⚡ Quick Start

### 1. Install Dependencies

```bash
pip install tensorflow opencv-python matplotlib kagglehub
```

### 2. Download CelebA Dataset

```python
import kagglehub
celeba_dataset_path = kagglehub.dataset_download('jessicali9530/celeba-dataset')
```

### 3. Train the Model

---

## 🔬 How It Works

1. **Encoder:** Extracts hierarchical features from low-res images.
2. **Bottleneck:** Captures deep representations at the smallest spatial scale.
3. **Decoder:** Upsamples features with skip connections for high-res reconstruction.
4. **Extra Upsampling:** Expands output from 64x64 → 512x512 seamlessly.

---

## 🚀 Next-Level Improvements

* **Loss Functions:** Perceptual loss or SSIM loss for sharper outputs.
* **Data Diversity:** Incorporate more datasets for robustness.
* **GANs:** Use Generative Adversarial Networks for photo-realistic super-resolution.
* **Hyperparameter Tuning:** Optimize filters, dropout, learning rate, and batch size.

---

## 💼 Who Is This For?

* ML enthusiasts looking to explore **image super-resolution**.
* Researchers wanting a **lightweight U-Net baseline**.
* Developers aiming to **enhance image quality** in photo apps, games, or media pipelines.

---

## 📜 License

This project is **MIT licensed**, feel free to use, modify, and expand.