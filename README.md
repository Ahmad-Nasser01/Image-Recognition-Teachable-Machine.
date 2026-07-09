# Lion vs. Tiger Image Classification Project

This repository contains a complete, lightweight end-to-end Image Classification project. The goal is to accurately distinguish between images of **Lions** and **Tigers** using deep learning transfer learning concepts, trained via Google's Teachable Machine and deployed through a Python script.

## 1. Dataset & Model Training
Using Google's Teachable Machine, I created a custom dataset with two distinct classes:
* **Class 1:** Lion (5 sample images)
* **Class 2:** Tiger (5 sample images)

The model was trained directly in the browser, evaluating features from the training samples to find patterns that distinguish the two animals.

<img width="1306" height="697" alt="image" src="https://github.com/user-attachments/assets/3fe1b8be-c94d-48cb-b733-29d3e78cb4f8" />


## 2. Model Exportation
Once training achieved optimal training metrics, the model was exported in the **TensorFlow -> Keras** format. This generated two critical files included in this repository:
* `keras_model.h5`: Contains the trained weights and model architecture.
* `labels.txt`: Contains the indexed class names (`0 Lion`, `1 Tiger`).

## 3. Python Implementation & Preprocessing
The model was deployed using a Python script inside a Google Colab environment. To ensure accurate predictions, the script performs the following image preprocessing steps before feeding the image into the neural network:
1. **Resizing:** The input test image is resized to **224x224 pixels** to match the exact input shape expected by the trained network.
2. **Data Conversion:** The image is converted into a structured `numpy` array.
3. **Normalization:** Pixel values (originally 0-255) are normalized to a scale between **-1 and 1** using the formula `(image_array / 127.5) - 1`.

## 4. Verification & Final Results
To verify the system, a test image of a lion was passed through the pipeline. The script successfully executed the forward pass and outputted the correct classification:
* **Predicted Class:** Lion
* **Confidence Score:** 99.97% (`0.99975914`)

This high confidence score indicates that the model successfully extracted the core visual boundaries between the two categories.

<img width="553" height="85" alt="image" src="https://github.com/user-attachments/assets/51c9cf5c-5f7f-4bef-b4b9-7039725957f9" />


## Repository Files
* `keras_model.h5` - The exported Keras model weights.
* `labels.txt` - The class index file.
* `Untitled0.ipynb` - The complete Python code script for running predictions.
