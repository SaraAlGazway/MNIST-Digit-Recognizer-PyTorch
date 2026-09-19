# 🎯 MNIST Digit Recognizer - UltimateCNN

> A PyTorch CNN solution for the Kaggle Digit Recognizer competition (99.36% accuracy).

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red)
![Accuracy](https://img.shields.io/badge/Accuracy-99.36%25-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📋 Overview

This project implements an **UltimateCNN** for the Kaggle Digit Recognizer competition (MNIST dataset).

| Property | Value |
|----------|-------|
| **Dataset** | MNIST (42,000 train + 28,000 test) |
| **Model** | UltimateCNN (Conv + BN + Dropout) |
| **Framework** | PyTorch |
| **Test Accuracy** | **99.36%** |
| **Parameters** | 468,458 |

---

## 🏗️ Architecture

Input (1×28×28) goes through two convolutional blocks:

**Block 1:** Conv → BN → ReLU → Conv → BN → ReLU → MaxPool → Dropout → (32×14×14)

**Block 2:** Conv → BN → ReLU → Conv → BN → ReLU → MaxPool → Dropout → (64×7×7)

Then Flatten (3136) → Classifier → Linear → BN → ReLU → Dropout → Linear (10) → Output (10 classes)

### Key Components

| Component | Purpose |
|-----------|---------|
| Conv2d | Extract spatial features |
| BatchNorm2d | Speed up + stabilize training |
| ReLU | Add non-linearity |
| MaxPool2d | Reduce dimensions |
| Dropout | Prevent overfitting |

---

## 📁 Project Structure

MNIST-Digit-Recognizer-PyTorch/
- README.md (Project documentation)
- requirements.txt (Dependencies)
- .gitignore (Git ignore rules)
- digit_recognizer.ipynb (Main notebook)
- submission.csv (Kaggle submission file)

---

## 🚀 Getting Started

### Prerequisites

pip install -r requirements.txt

### Installation

git clone https://github.com/SaraAIGazway/MNIST-Digit-Recognizer-PyTorch.git
cd MNIST-Digit-Recognizer-PyTorch
pip install -r requirements.txt

### Run the Notebook

jupyter notebook digit_recognizer.ipynb

---

## 📊 Results

### Training Progress

| Epoch | Loss | Accuracy |
|-------|------|----------|
| 1 | 0.1932 | 95.32% |
| 5 | 0.0392 | 98.80% |
| 10 | 0.0273 | 99.15% |
| 15 | 0.0207 | **99.36%** |

### Final Metrics

| Metric | Value |
|--------|-------|
| Test Accuracy | **99.36%** |
| Parameters | 468,458 |
| Training Time | ~2 min (GPU) |
| Framework | PyTorch |

---

## 🧠 Model Details

### Feature Extraction

| Layer | Type | Output Shape |
|-------|------|--------------|
| Input | Image | 1×28×28 |
| Block 1 | Conv + BN + ReLU × 2 | 32×14×14 |
| Block 2 | Conv + BN + ReLU × 2 | 64×7×7 |
| Flatten | View | 3136 |

### Classifier

| Layer | Type | Output Shape |
|-------|------|--------------|
| FC1 | Linear(3136, 128) | 128 |
| BN | BatchNorm1d | 128 |
| ReLU | Activation | 128 |
| Dropout | 0.5 | 128 |
| FC2 | Linear(128, 10) | 10 |

---

## 🎓 Key Takeaways

1. Data Augmentation improves generalization
2. Batch Normalization speeds up training
3. Dropout prevents overfitting
4. CNN outperforms MLP for image tasks
5. Data Augmentation helps the model generalize better

---

## 🚀 Future Improvements

- Ensemble models for higher accuracy
- Test-Time Augmentation (TTA)
- Learning rate scheduling
- More epochs (20-30)
- Try different optimizers (SGD + momentum)

---

## 📚 References

- Kaggle Digit Recognizer: https://www.kaggle.com/competitions/digit-recognizer
- PyTorch Docs: https://pytorch.org/docs/stable/nn.html
- MNIST Dataset: http://yann.lecun.com/exdb/mnist/
- Batch Normalization Paper: https://arxiv.org/abs/1502.03167
- Dropout Paper: https://jmlr.org/papers/v15/srivastava14a.html

---

## 👨‍💻 Author

**Sara AIGazway**

- GitHub: https://github.com/SaraAIGazway
- Kaggle: https://www.kaggle.com/

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch (git checkout -b feature/AmazingFeature)
3. Commit your changes (git commit -m 'Add some AmazingFeature')
4. Push to the branch (git push origin feature/AmazingFeature)
5. Open a Pull Request

---

## ⭐ Show your support

Give a ⭐️ if this project helped you!

---

## 📝 License

This project is licensed under the MIT License.

---

Made with ❤️ by Sara AIGazway
