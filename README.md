# XAI for Cat vs Dog Classification
> Explainable AI implementation to understand deep learning model predictions

## Table of Contents
- [Overview](#overview)
- [Links](#links)
- [Technologies](#technologies)
- [Setup](#setup)
- [Usage](#usage)
- [XAI Methods](#xai-methods)
- [Results](#results)
- [Team](#team)

## Overview
This project applies **Explainable AI (XAI)** techniques to a cat vs dog image classifier. We trained an EfficientNetV2-S model and used 4 different XAI methods to explain its predictions.

**Key Features:**
- EfficientNetV2-S classifier with 97% accuracy
- 4 XAI methods: Grad-CAM, LIME, Occlusion, Integrated Gradients
- Analysis of 6 samples comparing all methods

## Links
- [Training Notebook](https://colab.research.google.com/drive/1U9Gqai1guDB4mCcOQRu3rsXbuvkFPTRw?usp=sharing)
- [XAI Analysis Notebook](https://colab.research.google.com/drive/1toxHsEVZHK7IlMFYAAbZuaT3sXrJo6y0?usp=sharing)
- [Trained Model](https://drive.google.com/file/d/1_9jwIS4-2hxkKq6qzzn2T0VLe7nlKZi2/view?usp=sharing)
- [Dataset](https://drive.google.com/drive/folders/1Bo_qGPwjxQ9xxmjccvVA4S78yCorNwp2?usp=sharing)

## Technologies
- **Framework:** PyTorch, TorchVision
- **Model:** EfficientNetV2-S (pretrained on ImageNet)
- **XAI Libraries:** Captum, LIME
- **Tools:** NumPy, Pandas, Matplotlib, OpenCV

## Setup

1. **Install dependencies**
    ```bash
    pip install --upgrade pip
    pip install -r requirements.txt
    pip3 install torch torchvision
    ```

2. **Run the notebooks**
    - Run all cells

## Usage

### Using Google Colab (Easiest)
1. Open [XAI Analysis Notebook](https://colab.research.google.com/drive/1toxHsEVZHK7IlMFYAAbZuaT3sXrJo6y0?usp=sharing)
2. Run all cells
3. See visualizations for all 4 XAI methods

### Running Locally
1. Open src/XAI_ANALYSIS_13522061_13522075.ipynb
2. Setup kernels for .ipynb
3. Run the cells

## XAI Methods

### 1. Grad-CAM
- **What it does:** Creates heatmaps showing which image regions are important
- **Speed:** Fast
- **Best for:** Quick overview of model focus

### 2. LIME
- **What it does:** Segments image and highlights important parts
- **Speed:** Moderate
- **Best for:** Detailed explanations that are easy to understand

### 3. Occlusion
- **What it does:** Blocks parts of the image to see which affect prediction most
- **Speed:** Slow
- **Best for:** Validating that model focuses on correct features

### 4. Integrated Gradients
- **What it does:** Precise attribution using gradient integration
- **Speed:** Moderate
- **Best for:** Research and formal analysis

## Results

**Model Performance:**
- Validation Accuracy: 97.5%
- F1-Score: 0.975
- Dataset: Cat and Dog images from IF3270 Praktikum

**Key Findings:**
1. Model correctly focuses on facial features (eyes, nose, ears)
4. Model struggles with unusual poses and cluttered backgrounds


## Team

**Maximilian Sulistiyo**  
NIM: 13522061  
GitHub: [riyorax](https://github.com/riyorax)

**Marvel Pangondian**  
NIM: 13522075  
GitHub: [MarvelPangondian](https://github.com/MarvelPangondian)

---

**Course:** IF4070 Knowledge Representation and Reasoning
**Institution:** Institut Teknologi Bandung  
**License:** MIT
