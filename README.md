# Hybrid Automatic License Plate Detection and Recognition (ALPD)

A deep learning–based Hybrid Automatic License Plate Detection and Recognition (ALPD) system that combines **YOLOv5**, **YOLOv8n**, **Weighted Boxes Fusion (WBF)**, and **EasyOCR** for accurate and robust license plate detection and text recognition from vehicle images and videos.

---

# 🚀 Features

- Hybrid detection using **YOLOv5 + YOLOv8n**
- Improved localization using **Weighted Boxes Fusion (WBF)**
- OCR-based license plate recognition using **EasyOCR**
- Image and video inference support
- Real-time capable detection pipeline
- Automatic plate cropping and preprocessing
- Evaluation metrics and visualization support
- Supports custom datasets

---

# 🧠 Project Pipeline

```text
Input Image/Video
        ↓
YOLOv5 Detection
        ↓
YOLOv8n Detection
        ↓
Weighted Boxes Fusion (WBF)
        ↓
License Plate Cropping
        ↓
Image Preprocessing
        ↓
EasyOCR Recognition
        ↓
Text Postprocessing
        ↓
Final License Plate Output
```

---

# 🛠️ Technologies Used

- Python
- PyTorch
- YOLOv5
- YOLOv8 (Ultralytics)
- OpenCV
- EasyOCR
- NumPy
- Matplotlib
- Weighted Boxes Fusion
- Google Colab

---

# 📂 Dataset

The project uses a custom/annotated license plate dataset in YOLO format.

Dataset preparation includes:
- Annotation conversion
- Train/Validation/Test split
- YOLO format labeling
- Data preprocessing

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/your-username/hybrid-alpd.git
cd hybrid-alpd
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 📦 Required Libraries

```bash
pip install ultralytics
pip install torch torchvision
pip install easyocr
pip install opencv-python
pip install ensemble-boxes
pip install matplotlib
pip install numpy
```

---

# ▶️ Running the Project

## Open Notebook

Run the notebook:

```bash
ALPD_AG_2.ipynb
```

using:
- Jupyter Notebook
- Google Colab

---

# 🧪 Training

## YOLOv5 Training

```python
python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt
```

---

## YOLOv8n Training

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")

model.train(
    data="dataset.yaml",
    epochs=50,
    imgsz=640
)
```

---

# 🔍 Inference

The system:
1. Detects license plates using YOLOv5 and YOLOv8n
2. Fuses detections using WBF
3. Crops detected plates
4. Applies OCR preprocessing
5. Extracts text using EasyOCR
6. Displays final results

---

# 📊 Evaluation Metrics

The project evaluates:
- Precision
- Recall
- F1-score
- mAP@50
- mAP@50-95
- IoU-based detection accuracy

---

# 📸 Output Example

```text
Detected Plate: WB06A1234
Confidence: 0.96
```

---

# 📁 Repository Structure

```text
├── ALPD_AG_2.ipynb
├── dataset/
├── models/
├── outputs/
├── weights/
├── README.md
├── requirements.txt
```

---

# 🔬 Key Techniques Used

- Hybrid Object Detection
- Weighted Boxes Fusion
- OCR-based Text Recognition
- Image Enhancement
- Adaptive Thresholding
- Morphological Operations

---

# ✅ Advantages of the Hybrid Model

- Better detection accuracy
- Reduced false positives
- Improved small object detection
- Enhanced OCR performance
- Robust under varying lighting conditions
- Faster and more reliable than single-model systems

---

# 📈 Future Improvements

- Real-time deployment on edge devices
- Multi-country plate recognition
- Tracking-based vehicle monitoring
- Integration with traffic surveillance systems
- Deployment using Flask/Streamlit

---

# 👨‍💻 Author

Developed as a Final Year AI/ML Project on Hybrid Automatic License Plate Detection and Recognition using Deep Learning and OCR.

---

# 📜 License

This project is intended for academic and research purposes.
