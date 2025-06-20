# 💷 UK Coin Count Detection using YOLOv8

This project aims to solve two real-world vision tasks using unlabelled images of coins:
- **Q1**: Estimate the total **sterling value** of coins per image (UK coins only).
- **Q2**: Count the number of **‘heads’** visible per image.

The tasks are tackled using a **YOLOv8-based object detection model**, combined with custom datasets and transfer learning.

---

## 📂 Dataset Overview

We use two datasets:
- **DB1**: Clean and simple coin images.
- **DB2**: Complex backgrounds and real-world variations.

Since both are unlabelled, we manually annotated 100+ images using [Roboflow](https://roboflow.com), then applied augmentation for robust model training.

---

## 🔍 Exploratory Data Analysis (EDA)

Basic EDA includes:
- Image counts and shapes
- Channel information
- Visual previews

---

## 🚀 Model Training

We use YOLOv8 for both Q1 and Q2 due to its high performance on small datasets.

### 🛠️ Q1: Coin Type Detection
- Train a YOLOv8 model to detect **UK coins only**.
- Predict on DB1 and DB2.
- Convert detected coins to total value.

📈 **Training Stats**  
> _Insert YOLO training graph here_  
> `![YOLOv8 Training](runs\train_DB1\coin_value_v8n3\results.png)`

---

### 🎯 Q2: Head/Tail Classification
- Train another YOLOv8 model to detect **coin orientation** (head or tail).
- Generate counts per image for Q2 analysis.

📈 **Training Stats**  
> _Insert YOLO training graph here_  
> `![YOLOv8 Training](runs\train_heads_vs_tails\yolo_heads_tails_final\results.png)`

---

## 📊 Results

### Q1: Total Sterling Value Per Image
> _Insert prediction sample & plot_  
> `![Original image - DB1](Data\dataset1\coins1.png)`  
> `![Predicted coins value - DB1](runs\predict\dataset1_results\coins1.jpg)`

### Q2: Number of Heads Per Image
> _Insert prediction sample & plot_  
> `![original image - DB1](Data\dataset2\coins72.png)`  
> `![Predicted Head Count - DB1](runs\predict\Q2\dataset2_results_extra\coins72.jpg)`

---

## 🧪 How to Reproduce

1. Clone this repo and install dependencies:
   ```bash
   git clone https://github.com/yourusername/uk-coin-count.git
   cd uk-coin-count
   pip install -r requirements.txt
