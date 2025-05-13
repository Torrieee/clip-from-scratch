# 🔗 CLIP from Scratch (Minimal Implementation)

This repository provides a minimal PyTorch implementation of [CLIP (Contrastive Language–Image Pretraining)](https://arxiv.org/abs/2103.00020), inspired by OpenAI's original work. It is designed for educational purposes to help understand how image-text contrastive learning works from the ground up.

---

## 📌 Features

- ResNet-based **Image Encoder**
- Transformer-based **Text Encoder**
- Contrastive loss for **image-text alignment**
- Simple training loop with PyTorch
- Easy-to-modify for custom datasets

---

## 🧠 Model Architecture

- **Image Encoder**: ResNet18 (pretrained on ImageNet) + projection head
- **Text Encoder**: Transformer (positional embeddings + 6 layers)
- **Loss**: Symmetric cross-entropy between image and text embeddings

---

## 🛠️ Installation

```bash
git clone https://github.com/Torrieee/clip-from-scratch.git
cd clip-from-scratch
pip install -r requirements.txt
