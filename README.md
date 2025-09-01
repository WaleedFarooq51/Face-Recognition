# Face Recognition using Siamese Network (VGG-16 + Triplet Loss)

This repository contains a **Face Recognition Model** built by fine-tuning **VGG-16** and training it in a **Siamese Network architecture** with a **Triplet Loss function**.  
The model is designed to learn discriminative embeddings for face verification and recognition tasks.

---

## 🚀 Features
- Fine-tuned VGG-16 backbone for feature extraction.
- Siamese Network architecture for face comparison.
- Training with Triplet Loss to improve embedding space separation.
- Generates embeddings for faces that can be compared using distance metrics.
- Useful for Face Verification and Face Identification.

---

## Evaluation

If you want to evaluate the model on your own test images, run the `Real-time-prediction.ipynb` colab notebook, which loads the model checkpoints, stored in this [link]() and also provides instructions for collecting gallery and probe images for testing.

## Training from scratch

If you wish to train your model and get your own weights, then you can use `SiameseNetwork-TripletLoss.ipynb` colab notebook. Obviously, it is a Transfer learning technique, so the weights for the VGG-16 model can be downloaded from [here]() and then can be used to fine-tune the model.

## Training Data

- The VGGFace2 dataset, consisting of 8631 distinct celebrity images, is used for fine-tuning the VGG-16 model used above. Fine-tune the model using the VGGFace2 dataset       available [here]() and test it on your own family members and friends images.

- The frontal face detector provided by the dlib library is used, and after that, the images are sent to the `preprocess_input function`. The dlib’s frontal face detector is   used to detect images containing faces and store the dataset in a different folder named `training dataset` folder, execute `DataGeneration.ipynb`, which is then used to     fine-tune the model.
