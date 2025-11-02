# 🧠 Handwritten Digit Classification with PyTorch

This project implements a **Neural Network (NN)** from scratch using **PyTorch** to classify handwritten digits from the **MNIST dataset**.
It includes dataset preprocessing, model design, training, evaluation, and saving the trained model — providing a full learning pipeline for beginners and enthusiasts in deep learning.

---

## 📂 Project Structure

* **Project_9.1_(a).ipynb** → Dataset loading, exploration, preprocessing, and visualization
* **Project_9.1_(b).ipynb** → Neural network creation, training, and evaluation
* **mnist_model_state_dict.pth** → Saved trained model weights
* **mnist_train_processed.pth** → Preprocessed training dataset
* **mnist_test_processed.pth** → Preprocessed test dataset

---

## ⚙️ Key Steps

### 🧩 Data Preprocessing

* Converted images to tensors and normalized pixel values
* Flattened images (1, 28, 28) → 784-dimensional vectors

### 🧠 Model Architecture

* Input Layer → 784 neurons
* Hidden Layer 1 → 128 neurons with ReLU activation
* Hidden Layer 2 → 64 neurons with ReLU activation (for experiment)
* Output Layer → 10 neurons (representing digits 0–9)

### 🔧 Training Setup

* **Loss Function:** CrossEntropyLoss
* **Optimizer:** Adam with custom learning rate
* **Epochs:** 5
* **Batch Size:** 64

---

## 📊 Evaluation Metrics

After training, model performance was measured using:

* Accuracy
* Precision
* Recall
* F1-Score

Results showed strong performance on the MNIST test set, with steady convergence and balanced precision-recall behavior.

---

## 💾 Model Saving and Loading

The trained model is saved as **mnist_model_state_dict.pth**.
You can reload and evaluate the model using:

```python
model.load_state_dict(torch.load('model_state.pth'))
model.eval()
```

---

## 🚀 Future Improvements

* Add **Convolutional Layers (CNNs)** for better spatial feature extraction
* Implement **Dropout** or **Batch Normalization** for generalization
* Deploy model with **Streamlit** or **Flask** for real-time prediction

---

## 👨‍💻 Author

**BROWN BOY**
BS in Computer Science | Aspiring Machine Learning and Deep Learning Researcher

---

## ⭐ Support

If you find this project helpful, please **star 🌟 the repository** on GitHub to show your support!
