# Animal Classifier (Lion vs. Tiger)

A simple Machine Learning project that identifies whether an image contains a **Lion** or a **Tiger**. The model was trained using Google's Teachable Machine and deployed via a Python script.

## 1. Model Training (Teachable Machine)
I created two classes (`Lion` and `Tiger`), uploaded dataset samples, and trained the model. The model successfully learned to distinguish between the two animals.

<img width="1306" height="697" alt="image" src="https://github.com/user-attachments/assets/f9a4b891-7995-47da-9d12-f62c726f3669" />


## 2. Python Implementation & Results
After exporting the model in Keras format (`.h5`), I wrote a Python script in Google Colab to process input images and run predictions. 

As shown below, the model successfully detected the test image as a **Lion** with a **99.9% confidence score**:

<img width="553" height="85" alt="image" src="https://github.com/user-attachments/assets/1fecb3cd-c4fe-4a24-b07b-95258b097571" />


## How It Works
1. **Load:** The script loads the trained `keras_model.h5` and `labels.txt`.
2. **Process:** Images are resized to 224x224 pixels and normalized.
3. **Predict:** The model predicts the class and outputs the confidence percentage.

## Requirements
To run this project locally, install the following libraries:
```bash
pip install tensorflow pillow numpy
