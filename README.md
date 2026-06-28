# 😊 Face Expression Detection Using Deep Learning

A real-time **Face Expression Detection** system built using **Deep Learning**, **TensorFlow/Keras**, and **OpenCV**. The project detects human faces from a webcam feed and classifies facial expressions into one of seven emotion categories.

## 📌 Features

- 🎥 Real-time facial expression recognition using webcam
- 🧠 CNN-based deep learning model
- 👤 Face detection using OpenCV Haar Cascade
- 😊 Supports seven facial expressions
- ⚡ Fast inference with pre-trained model weights
- 📒 Easy-to-use Jupyter Notebook implementation

---

# 📂 Repository Structure

```text
Face-Expression-Detection-Using-Deep-Learning/
│
├── Face-Expression-Testing.ipynb
├── model.json
├── model_weights.h5
├── haarcascade_frontalface_default.xml
└── README.md
```

---

# 🧠 Model Architecture

The facial expression recognition model is based on a **Convolutional Neural Network (CNN)**.

### Network Components

- Convolutional Layers
- Batch Normalization
- ReLU Activation
- Max Pooling Layers
- Dropout Layers
- Fully Connected (Dense) Layers
- Softmax Output Layer

### Architecture Flow

```text
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

# 😀 Supported Facial Expressions

| Label | Emotion |
|-------|---------|
| 0 | Angry 😠 |
| 1 | Disgust 🤢 |
| 2 | Fear 😨 |
| 3 | Happy 😊 |
| 4 | Neutral 😐 |
| 5 | Sad 😢 |
| 6 | Surprise 😲 |

---

# ⚙️ Data Preprocessing

The input images undergo the following preprocessing steps before prediction:

- Resize images to **48 × 48**
- Convert to grayscale
- Normalize pixel values
- Face detection using Haar Cascade
- Prepare image for CNN inference

---

# 🚀 Model Training

The CNN model was trained using a labeled facial expression dataset.

### Training Configuration

| Parameter | Value |
|----------|-------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Batch Size | 128 |
| Epochs | 50 |
| Input Size | 48 × 48 |

### Data Augmentation

- Image Rescaling
- Rotation
- Width Shift
- Height Shift
- Horizontal Flip
- Zoom

The best-performing model weights were saved using **ModelCheckpoint**.

---

# 📊 Model Workflow

```text
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
Display Emotion Label
```

---

# 💻 Installation

## 1. Clone the repository

```bash
git clone https://github.com/KVSGVinayak11/Face-Expression-Detection-Using-Deep-Learning.git
```

## 2. Navigate to the project folder

```bash
cd Face-Expression-Detection-Using-Deep-Learning
```

## 3. (Optional) Create a virtual environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

## 4. Install dependencies

```bash
pip install tensorflow keras opencv-python numpy matplotlib jupyter
```

---

# ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook:

```text
Face-Expression-Testing.ipynb
```

Run all notebook cells sequentially.

The notebook will:

- Load the CNN model architecture (`model.json`)
- Load the trained weights (`model_weights.h5`)
- Initialize the webcam
- Detect faces using Haar Cascade
- Predict facial expressions
- Display the predicted emotion in real time

---

# 📦 Model Files

| File | Description |
|------|-------------|
| `model.json` | CNN model architecture |
| `model_weights.h5` | Trained model weights |
| `haarcascade_frontalface_default.xml` | OpenCV Haar Cascade face detector |
| `Face-Expression-Testing.ipynb` | Jupyter Notebook for real-time inference |

---

# 🛠️ Dependencies

- Python 3.9+
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

Install all dependencies:

```bash
pip install tensorflow keras opencv-python numpy matplotlib jupyter
```

---

# 📈 Applications

This project can be used in:

- Human-Computer Interaction (HCI)
- Smart Surveillance Systems
- Driver Monitoring Systems
- E-Learning Platforms
- Healthcare and Mental Wellness
- Customer Experience Analytics
- Robotics and Interactive AI

---

# 🚀 Deployment

The trained model can be deployed in:

- Desktop Applications
- Web Applications
- Edge Devices
- Real-Time Webcam Systems
- AI-powered Monitoring Systems

Deployment recommendations:

- Package the trained model with dependencies.
- Store model artifacts securely.
- Use GPU acceleration for faster inference.
- Containerize using Docker for production environments.

---

# 📊 Model Monitoring

For production deployment, monitor:

- Prediction accuracy
- Inference latency
- Model drift
- User feedback
- Data distribution changes

Retraining the model periodically with new data helps maintain performance over time.

---

# 🔮 Future Improvements

- Replace Haar Cascade with MTCNN or RetinaFace
- Implement Transfer Learning (EfficientNet, ResNet, MobileNet)
- Improve accuracy using Attention Mechanisms
- Export model to TensorFlow Lite or ONNX
- Deploy using Flask/FastAPI
- Build a Streamlit web application
- Mobile deployment for Android and iOS

---

# 🙏 Acknowledgements

- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- FER2013 Facial Expression Dataset
- Deep Learning Community

---

# 📄 License

This project is licensed under the **MIT License**.

---

# ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub.

---

<div align="center">

### Made with ❤️ using Deep Learning and Computer Vision

</div>
