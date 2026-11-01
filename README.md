# CNN-Based Receipt Fraud Detection (Real vs Fake)

This project explores binary receipt-image classification with a custom convolutional neural network (CNN) in PyTorch. The notebook describes image preparation, model training, and a Gradio image-upload interface.

## Notebook workflow

- Extract `receiptimages.zip` into the Colab workspace.
- Read receipt images from folders named `real` and `fake`.
- Resize images to 224 × 224 pixels and create training and validation datasets.
- Train a three-stage CNN and save model weights as `cnn_model.pth`.
- Use the Gradio interface to view a predicted class and score.

Labels are `REAL` and `FAKE`. Predictions are experimental model estimates and should not be treated as proof of fraud.

## Data

The notebook expects `receiptimages.zip` with `real` and `fake` image folders. The archive is not included. I could not verify a Kaggle dataset that both matches this receipt-image schema and clearly permits redistribution, so no substitute data has been added. Use a dataset whose license allows your intended use.

## Repository contents

- `CNN_Based_Receipt_Fraud_Detection.ipynb` — model, data preparation, and interface workflow.
- `README.md` — project overview and setup notes.

## Important execution note

The notebook calls `train.py` and `serve.py` and imports `ReceiptFraudCNN` from `model.py`, but those helper files are not present in this repository. The image archive is external as well, so the notebook is not currently self-contained. Add the helper files and provide the expected image archive before running the training and Gradio sections.

## Run in Google Colab

1. Open `CNN_Based_Receipt_Fraud_Detection.ipynb` in Google Colab.
2. Provide the expected image archive and verify its `real` and `fake` folder structure.
3. Resolve the references to `model.py`, `train.py`, and `serve.py`.
4. Install PyTorch, OpenCV, Gradio, and any other packages requested by the runtime.

Training time and model quality depend on the data, split, and configuration. No fixed accuracy is claimed.

## Author

Gizem Bektaş
