

# 😷 Face Mask Detection Web App

A simple and interactive **Face Mask Detection** app built with **TensorFlow**, **MobileNetV2**, and **Gradio**.  
It detects whether a person in an image is wearing a mask or not.  

The model is trained on a labeled dataset from Kaggle.  

---

## 📎 Dataset

The dataset used for training is available on Kaggle:

🔗 [Face Mask Detection Dataset](https://www.kaggle.com/datasets/debarghamitraroy/face-mask-detection)

- Organize the dataset into `train` and `validation` folders.
- Each folder should have two subfolders:
  - `mask`
  - `no_mask`

---

## 🧠 Model

- **Base model:** MobileNetV2 (pretrained on ImageNet)  
- **Input size:** 224×224 RGB images  
- **Output:** 2-class softmax (No Mask / Mask)  
- **Training:** Balanced dataset, proper preprocessing with `preprocess_input`  

---

## 🛠️ Features

- Detects Mask / No Mask in images with emoji labels.  
- Works on CPU (no GPU needed).  
- Handles BGR, RGB, and RGBA images automatically.  
- Easy-to-use web interface via **Gradio**.

---

## ⚡ Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/face-mask-detection.git
cd face-mask-detection

2.Create a virtual environment (optional but recommended):
python -m venv venv
# Linux / Mac
source venv/bin/activate
# Windows
venv\Scripts\activate

3.Install dependencies:
pip install -r requirements.txt

4.Place your trained model file mask_detector.h5 in the project root folder.

##🚀 Running the App
python app.py

A Gradio interface will open in your browser.
Upload any image to see the prediction.

##🧾 Example

Upload an image and get output like:

😷 Mask (98.23%)
❌ No Mask (1.77%)

##📦 Project Structure

face-mask-detection/
│
├── app.py                # Gradio app
├── mask_detector.h5      # Trained Keras model
├── requirements.txt      # Dependencies
└── README.md             # This file
