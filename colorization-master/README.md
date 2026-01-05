# Image Colorization using Deep Learning

A PyTorch implementation of deep learning models for automatic image colorization. This project utilizes state-of-the-art Convolutional Neural Networks (CNNs) to "hallucinate" plausible colors for grayscale images.

The project implements and compares two distinct model architectures:
1.  **ECCV16** (Zhang et al.): Focused on plausible color classification.
2.  **SIGGRAPH17** (Zhang et al.): Focused on real-time user-guided applications.

## 📋 Features
* **Automatic Colorization**: Converts single-channel grayscale images into 3-channel RGB images.
* **Dual Model Support**: Switch between ECCV16 and SIGGRAPH17 generators.
* **Pretrained Weights**: Automatically downloads pretrained weights from the original authors' S3 buckets.
* **GPU Acceleration**: Optional CUDA support for faster processing.
* **Visual Comparison**: Generates a side-by-side comparison of the input and outputs from both models.

## 🛠️ Installation

### 1. Install the zip

### 2. Install dependecies
```bash
pip install -r requirements.txt
```


## Project Structure
```
├── colorizers/              # Package folder for model definitions
│   ├── __init__.py          # (Empty file) Makes this a python package
│   ├── base_color.py        # BaseColor class
│   ├── eccv16.py            # ECCVGenerator class
│   ├── siggraph17.py        # SIGGRAPHGenerator class
│   └── util.py              # load_img, resize_img, etc.
├── main.py                  # Entry point script (argparse & execution)
├── requirements.txt         # List of dependencies
└── README.md                # This file
```


## How to run
```bash
python main.py -i imgs/test_image.jpg
```