# CNN-Based Receipt Fraud Detection (Real vs Fake)

This project explores binary receipt-image classification with a custom convolutional neural network (CNN) implemented in PyTorch. The notebook prepares image paths, builds a balanced real/fake dataset, trains the model, and includes an image-upload prediction interface using Gradio.

## Notebook workflow

- Extract `receiptimages.zip` into the Colab workspace.
- Read receipt images from folders named `real` and `fake`.
- Resize images to 224 × 224 pixels and create training and validation datasets.
- Train a three-stage CNN with PyTorch and save model weights as `cnn_model.pth`.
- Use the Gradio interface to submit an image and view the predicted class and score.

Labels in the notebook are `REAL` and `FAKE`. The predictions are outputs of an experimental image classifier and should be interpreted as model estimates.

## Data

Provide `receiptimages.zip` in the Colab runtime. Its extracted directory should contain image folders named `real` and `fake`. The image archive is not included in this repository.

## Current repository contents

- `CNN_Based_Receipt_Fraud_Detection.ipynb` — model definition, data preparation, and interface code.
- `README.md` — project overview and usage notes.

## Important execution note

The notebook currently calls `train.py` and `serve.py` and imports `ReceiptFraudCNN` from `model.py`, but those helper files are not present in this repository. The image archive is also external. As committed, the notebook is therefore not a self-contained, ready-to-run demo; add or generate the referenced helper files and provide the dataset before running the training and interface cells.

## Run in Google Colab

1. Open `CNN_Based_Receipt_Fraud_Detection.ipynb` in Google Colab.
2. Provide the expected image archive and verify its `real` and `fake` folder structure.
3. Resolve the referenced helper scripts (`model.py`, `train.py`, and `serve.py`) before running the training and Gradio cells.
4. Install PyTorch, OpenCV, Gradio, and any other packages requested by the runtime.

Training uses a configurable number of epochs and an image dataset; runtime and model quality depend on the data, split, and settings. No fixed accuracy is claimed here.

## Author

Gizem Bektaş
