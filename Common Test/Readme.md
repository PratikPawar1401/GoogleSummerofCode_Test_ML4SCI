# Multiclass Classification Common Test
This repository contains a PyTorch implementation of a deep learning pipeline for classifying gravitational lensing effects. The model is trained to distinguish between three classes of lensing: no lensing (`no`), spherical lensing (`sphere`), and vortex/complex lensing (`vort`).

## How It Works

The pipeline takes gravitational lensing images (stored as NumPy arrays), processes them through a transfer learning model (default: ResNet18, optimized: EfficientNet-B0), and classifies them into three categories. The model uses a custom classification head with dropout regularization.

Training includes comprehensive logging, checkpointing based on validation AUC, and visualization of performance metrics (confusion matrices, ROC curves, and training history).

## Results
![roc_curve](https://github.com/user-attachments/assets/2dc9b3da-b8c5-4c01-a772-71e34382c787)
*ROC curve showing the model's performance on the test dataset.*

![training_history(3)](https://github.com/user-attachments/assets/ec572c70-e34b-4993-b51e-79696f3f7d6f)
Training and validation loss (left) and AUC (right) over training epochs.*


## Future Improvements

I'm actively working on enhancing this project. Here's my roadmap for future improvements:

### Data Handling & Augmentation
- [ ] Implement test-time augmentation for more robust predictions
- [ ] Add caching for faster data loading

### Model Architecture
- [ ] Experiment with astronomy-specific architectures
- [ ] Add attention mechanisms to focus on important features
- [ ] Test ensemble methods for improved accuracy

### Validation & Evaluation
- [ ] Implement Grad-CAM for model interpretability

### Engineering Improvements
- [ ] Add experiment tracking (MLflow or W&B)
- [ ] Create configuration file system
