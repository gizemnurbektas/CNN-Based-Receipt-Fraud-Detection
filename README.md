# CNN-Based Receipt Fraud Detection (Real vs Fake)

This project is a **CNN-based image classification application** developed to detect **manipulation or fraud suspicion** in receipt and payment slip images.  
The model is trained using **REAL (original)** and **FAKE (manually manipulated or scribbled)** receipt images and can be tested interactively via a **Gradio** web interface.

---

## Project Objective
The goal of this project is to develop a deep learning model capable of automatically detecting visual manipulations in receipt and banking document images, addressing common fraud-related issues in the banking and financial domain.

---

## Technologies Used
- Python  
- PyTorch  
- Convolutional Neural Networks (CNN)  
- OpenCV  
- Gradio  

---

## Input / Output
- **Input:** Receipt or payment slip image (JPG / PNG)  
- **Output:**  
  - `REAL (Original)`  
  - `FAKE (Manipulation Suspicion)`  
  - Confidence score (probability)

---

## Project Structure
The project follows the directory structure below:

receipt_fraud_cnn/
│
├── model.py # CNN model architecture
├── train.py # Model training script
├── serve.py # Gradio web interface
│
├── cnn_model.pth # Trained model (generated after training)
│
└── data/
└── receiptimages/
├── real/ # Original receipt images
└── fake/ # Manipulated / scribbled receipt images

## Installation
This project is designed to run on **Google Colab**.

Model Training

To train the model, run:

python train.py


After training, the model weights will be saved as cnn_model.pth.

Gradio Demo (Live Interface)

To launch the Gradio interface:

python serve.py


After execution, the terminal will display a message similar to:

Running on public URL: https://xxxxxx.gradio.live


Open the generated link to:

Upload receipt images

View REAL / FAKE predictions in real time

Demo Scenario

Upload an original receipt → the model predicts REAL

Upload a manipulated receipt → the model predicts FAKE

Perform 2–3 example tests to complete the presentation

Labeling

REAL (1) → Original receipt

FAKE (0) → Manipulated receipt

Notes

The FAKE class is created using manually altered receipt images.

This project is intended for educational and demonstration purposes.

For real-world deployment, training on a larger and more diverse dataset is recommended.
