# Grocery Store CNN  

![Python](https://img.shields.io/badge/Python-3.x-blue) ![PyTorch](https://img.shields.io/badge/PyTorch-1.x-orange) ![License](https://img.shields.io/badge/License-MIT-yellow)  

## 📋 Overview  
This project develops a product classification system for grocery store shelves using CNNs, aiding customer assistance and visually impaired individuals.  

## 🎯 Objectives  
- **Single Product Classification**: Identify products from images.  
- **Optimization**: Improve performance by fine-tuning ResNet-18.  

## 🖼️ Image Preprocessing  
- **Resizing & Cropping**: Images scaled to 224x224 px.  
- **Data Augmentation**: Flip, rotation, and color jitter for robustness.  

## 🧩 Initial Model  
The **GroceryModelFull**, inspired by VGG, includes:  
- 3 convolutional blocks with pooling.  
- Global Average Pooling to reduce complexity.  

### 🔬 Ablation Study  
Variations tested to assess model components:  
- **NoBN**: Without Batch Normalization.  
- **LessChannels**: Reduced channels.  
- **LessConvs**: One convolution per block.  
- **LessBlocks**: Only two convolutional blocks.  

## 🔥 Fine-Tuning ResNet-18  
The pre-trained model was adapted to **GroceryStoreDataset** in two stages:  
1. **Initial Fine-Tuning** with the best parameters from Part 1.  
2. **Further Adjustments** to achieve 80%-90% accuracy.  

### 🔧 Optimizations  
- **FC with Dropout (0.3)** to reduce overfitting.  
- **Batch size reduction (64 → 32)** for increased variability.  

## 📊 Results  
These adjustments improved model generalization, achieving the target validation accuracy.  
