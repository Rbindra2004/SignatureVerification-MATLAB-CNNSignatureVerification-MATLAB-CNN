# SignatureVerify-CNN

A CNN-based handwritten signature verification system developed in MATLAB. The model achieves up to **91–92% accuracy** on a publicly available signature dataset, outperforming deeper networks like ResNet, AlexNet, and VGG16 in this specific task.

## 📊 Dataset

The dataset used is from Kaggle:  
[Handwritten Signatures – Divyansh Rai](https://www.kaggle.com/datasets/divyanshrai/handwritten-signatures)

It contains genuine and forged signatures in RGB and grayscale formats across multiple users. Preprocessing was necessary to handle image format inconsistencies.

## 🧠 Model Architecture

Contrary to expectation, deeper pre-trained networks (ResNet, AlexNet, VGG16) yielded only 50–60% accuracy. A **simple 3-layer CNN** performed significantly better, likely due to the nature of the task and the dataset size.

The final CNN includes:
- Convolutional layers with ReLU activation
- Max pooling layers
- Fully connected layer
- Softmax classification

## 🔧 Key Improvements

- Unified all input images to grayscale to eliminate inconsistencies.
- Instead of using standard `[255 255]` input dimensions, dynamically resized input to match actual image dimensions.
- This change alone boosted accuracy from ~70% to **91–92%**.
- Built a custom UI in MATLAB for dataset selection, training, and prediction.

## 💻 Features

- MATLAB-based GUI for easy interaction
- High accuracy signature classification
- Custom preprocessing for better consistency and results

## 📂 File Structure

- `main_app.mlapp` – GUI for the project
- `cnn_model.m` – Custom CNN architecture
- `preprocess.m` – Image processing and resizing
- `train_model.m` – Script to train the network
- `README.md` – Project documentation

## 🧪 Accuracy

| Model     | Accuracy |
|-----------|----------|
| ResNet    | ~55%     |
| AlexNet   | ~60%     |
| VGG16     | ~58%     |
| **Custom CNN (3-layer)** | **91–92%** |

## 🚀 Getting Started

1. Clone the repository.
2. Open `main_app.mlapp` in MATLAB.
3. Ensure the dataset is placed in the correct folder structure.
4. Run the app to start training or testing the model.

---

> This project demonstrates how a simple architecture, paired with the right preprocessing, can outperform complex networks for domain-specific tasks.

