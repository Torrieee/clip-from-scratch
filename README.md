# CLIP from Scratch (Minimal Implementation)

This repository provides a minimal PyTorch implementation of [CLIP (Contrastive Language–Image Pretraining)](https://arxiv.org/abs/2103.00020), inspired by OpenAI's original work. It is designed for educational purposes to help understand how image-text contrastive learning works from the ground up.

---

## Features

- ResNet-based **Image Encoder**
- Transformer-based **Text Encoder**
- Contrastive loss for **image-text alignment**
- Simple training loop with PyTorch
- Easy-to-modify for custom datasets

---

## Model Architecture

- **Image Encoder**: ResNet18 (pretrained on ImageNet) + projection head
- **Text Encoder**: Transformer (positional embeddings + 6 layers)
- **Loss**: Symmetric cross-entropy between image and text embeddings

---

## Installation
```
git clone https://github.com/Torrieee/clip-from-scratch.git
cd clip-from-scratch
pip install -r requirements.txt
```

## Training
You can train the CLIP model on your own dataset of (image, text) pairs.

```
python train.py
```
Make sure to customize the data/dataloader.py and config.yaml to match your dataset.

🔍 Inference (Zero-shot matching)
```
python inference.py --image_path demo.jpg --text "a cat", "a dog", "a man in suit"
```
This will return which description best matches the image.

## Project Structure
clip-from-scratch/
│
├── models/               # Encoders & CLIP model
├── data/                 # Custom dataset loader
├── train.py              # Training script
├── inference.py          # Simple inference script
├── utils.py              # Helper functions & loss
├── config.yaml           # Model & training configuration
├── requirements.txt      # Dependencies
└── README.md             # You're here!
## Example Result
Coming soon: demo with toy dataset or Flickr8k/COCO captions.

## Reference
CLIP: Learning Transferable Visual Models From Natural Language Supervision, Radford et al. (OpenAI)

## Contact
Feel free to open an issue or reach out if you have questions or ideas!

Star this repo if you find it helpful!
