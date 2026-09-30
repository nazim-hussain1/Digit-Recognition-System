# Improved Handwritten Digit Recognizer

An enhanced Convolutional Neural Network (CNN) for handwritten digit classification (0–9), trained on the MNIST dataset.  
This version includes a stronger model architecture, data augmentation, robust real-world image preprocessing, and an interactive **Gradio** interface for instant predictions.

**Live Colab Notebook:** [Open in Google Colab](https://colab.research.google.com/drive/1nBrMb5h8VKjp7QSOGCg9aPRyTyz7t4gi?usp=sharing)

---

## Features

- Deeper CNN with Batch Normalization and Dropout
- Data augmentation (rotation, zoom, shifts) for better generalization
- Advanced preprocessing for real photos:
  - Auto-inversion (handles dark/light backgrounds)
  - Otsu thresholding
  - Digit centering + padding (MNIST-style)
- Interactive Gradio UI:
  - Upload image
  - Draw digit
  - Webcam support
  - Shows top predictions with confidence scores
- Test accuracy typically **> 99%**

---

## Model Architecture

- 2× Conv2D (32 filters) + BatchNorm + MaxPooling + Dropout
- 2× Conv2D (64 filters) + BatchNorm + MaxPooling + Dropout
- Dense (256) + BatchNorm + Dropout
- Softmax output (10 classes)

**Training details:**
- Optimizer: Adam
- Loss: Categorical Crossentropy
- Data Augmentation + EarlyStopping + ReduceLROnPlateau
- Epochs: up to 20 (with early stopping)

---

## Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- Gradio
- NumPy, Matplotlib, Pillow
- Google Colab

---

## How to Run

### Option 1: Google Colab (Recommended)
1. Open the [Colab Notebook](https://colab.research.google.com/drive/1nBrMb5h8VKjp7QSOGCg9aPRyTyz7t4gi?usp=sharing)
2. Runtime → Change runtime type → GPU (optional but faster)
3. Run all cells in order
4. Use the Gradio interface at the end to test your own digits

### Option 2: Locally
```bash
git clone https://github.com/nazim-hussain1/Digit-Recognition-System.git
cd Digit-Recognition-System
pip install tensorflow opencv-python gradio pillow matplotlib
# Then open the notebook in Jupyter / VS Code
