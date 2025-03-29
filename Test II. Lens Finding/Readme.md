# Gravitational Lens Finder

This project uses deep learning to automatically identify gravitational lensing phenomena in astronomical images.

## What This Project Does

The model distinguishes between images containing gravitational lenses and those without, using a transfer learning approach with state-of-the-art convolutional neural networks.

### Key Features

- **Transfer Learning Architecture**: Leverages pre-trained models (ResNet, DenseNet, EfficientNet, MobileNet) with customized classification layers for astronomical image analysis
- **Advanced Data Processing**: Implements image augmentation and normalization techniques optimized for astronomical data
- **Class Imbalance Handling**: Uses weighted sampling to ensure balanced training despite uneven class distributions
- **Comprehensive Evaluation**: Measures performance using ROC curves and AUC metrics with detailed visualizations

## How It Works

1. **Data Preparation**: Loads and preprocesses astronomical images, splitting them into training, validation, and test sets
2. **Model Configuration**: Sets up a transfer learning model with customizable hyperparameters
3. **Training Pipeline**: Implements a robust training process with learning rate scheduling and early stopping
4. **Evaluation**: Assesses model performance on held-out test data with detailed metrics

## Results

ResNet50 achieves excellent classification performance on test data, demonstrating the viability of automated gravitational lens detection.

### Performance Metrics
![test_roc_curve(1)](https://github.com/user-attachments/assets/8651960a-25c1-4242-b032-c69cc2687d99)
*ROC curve showing the model's performance on the test dataset.*

![training_history(2)](https://github.com/user-attachments/assets/202ebd95-0da4-4cc1-a0bb-3bcaa3d016e8)
*Training and validation loss (left) and AUC (right) over training epochs.*

## Future Improvements

- Implement Vision Transformer (ViT) architectures for potentially improved performance
- Add more diverse data augmentations specific to astronomical imagery
- Incorporate test-time augmentation for more robust predictions
- Implement model ensembling techniques to boost accuracy
