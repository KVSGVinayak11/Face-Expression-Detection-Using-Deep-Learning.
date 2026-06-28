# 😊 Face Expression Recognition using Deep Learning

A real-time **Face Expression Recognition** system built using **Convolutional Neural Networks (CNN)** and **OpenCV**. The model classifies human facial expressions into seven emotions:

- 😠 Angry
- 🤢 Disgust
- 😨 Fear
- 😊 Happy
- 😐 Neutral
- 😢 Sad
- 😲 Surprise

The application detects faces from a webcam feed, preprocesses them, and predicts the corresponding facial expression in real time.

---

# 📌 Features

- Real-time facial expression detection using webcam
- CNN-based deep learning model
- Face detection using OpenCV Haar Cascade
- Supports seven facial expressions
- Trained with data augmentation techniques
- Easy to deploy and extend

---

# 📂 Project Structure

```
Face-Expression-Recognition/
│
├── model/
│   ├── model.h5                 # Trained model
│   └── weights.h5               # Best model weights
│
├── haarcascade/
│   └── haarcascade_frontalface_default.xml
│
├── dataset/
│   ├── train/
│   └── validation/
│
├── src/
│   ├── train.py
│   ├── predict.py
│   └── model.py
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

# 🧠 Model Architecture

The facial expression classifier is built using a **Convolutional Neural Network (CNN)** consisting of:

- Convolutional Layers
- Batch Normalization
- ReLU Activation
- Max Pooling Layers
- Dropout Layers
- Fully Connected (Dense) Layers
- Softmax Output Layer

### Network Pipeline

```
Input Image (48×48×1)
        │
Conv2D + ReLU
        │
Batch Normalization
        │
MaxPooling
        │
Dropout
        │
Conv2D + ReLU
        │
Batch Normalization
        │
MaxPooling
        │
Dropout
        │
Conv2D + ReLU
        │
Flatten
        │
Dense Layer
        │
Dropout
        │
Dense Layer
        │
Softmax (7 Classes)
```

---

# 📊 Dataset

The model is trained on grayscale facial images of size **48 × 48 pixels**.

### Emotion Classes

| Class | Label |
|--------|-------|
| 0 | Angry |
| 1 | Disgust |
| 2 | Fear |
| 3 | Happy |
| 4 | Neutral |
| 5 | Sad |
| 6 | Surprise |

---

# ⚙️ Data Preprocessing

Before training, the following preprocessing steps were applied:

- Resize images to **48 × 48**
- Convert RGB images to grayscale
- Normalize pixel values
- Data augmentation:
  - Rescaling
  - Rotation
  - Width Shift
  - Height Shift
  - Horizontal Flip
  - Zoom

---

# 🚀 Model Training

### Optimizer

Adam

### Loss Function

Categorical Crossentropy

### Batch Size

128

### Epochs

50

### Callbacks

- ModelCheckpoint
- EarlyStopping *(optional)*
- ReduceLROnPlateau *(optional)*

Example training command:

```bash
python train.py
```

---

# 📈 Model Evaluation

The trained model is evaluated on a separate validation dataset using:

- Validation Accuracy
- Validation Loss
- Confusion Matrix *(optional)*
- Classification Report *(optional)*

---

# 💻 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Face-Expression-Recognition.git
```

Move into the project directory

```bash
cd Face-Expression-Recognition
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

Start real-time emotion detection:

```bash
python predict.py
```

The webcam will open and display the predicted facial expression for each detected face.

---

# 🛠️ Dependencies

- Python 3.x
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib

Install manually if needed:

```bash
pip install tensorflow opencv-python numpy matplotlib
```

---

# 📷 Workflow

```
Webcam Input
      │
Face Detection
(OpenCV Haar Cascade)
      │
Face Cropping
      │
Resize (48×48)
      │
Grayscale Conversion
      │
Normalization
      │
CNN Model
      │
Emotion Prediction
      │
Display Result
```

---

# 📦 Deployment

The trained model can be deployed for:

- Real-time webcam applications
- Smart surveillance systems
- Human-computer interaction
- Driver emotion monitoring
- Online learning platforms
- Healthcare and mental wellness systems

Deployment recommendations:

- Package the model with all dependencies.
- Store trained weights securely.
- Use GPU acceleration for faster inference.
- Containerize using Docker for production deployment.

---

# 📊 Model Monitoring

For production environments, monitor:

- Prediction accuracy
- Inference latency
- Model drift
- User feedback
- Data distribution changes

Retraining the model periodically with new data helps maintain high accuracy.

---

# 🔮 Future Improvements

- Use transfer learning (EfficientNet, ResNet, MobileNet)
- Replace Haar Cascade with MTCNN or RetinaFace
- Improve accuracy using attention mechanisms
- Export to TensorFlow Lite or ONNX
- Deploy using Flask/FastAPI
- Add support for video file processing
- Mobile deployment (Android/iOS)

---

# 📄 License

This project is licensed under the MIT License.

---

# 🙏 Acknowledgements

- TensorFlow / Keras
- OpenCV
- FER2013 Dataset
- Deep Learning Community

---

# ⭐ If you found this project useful, consider giving it a star!

```
Made with ❤️ using Deep Learning and Computer Vision
```
