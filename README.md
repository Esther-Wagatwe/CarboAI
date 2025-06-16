# 🥗 CarboAI: Carbohydrate Estimation from Food Images

CarboAI is a deep learning pipeline designed to estimate the **carbohydrate content** of food items directly from images. By combining **YOLOv8 object detection** with a **custom neural network**, this model detects food in an image, extracts visual features, and predicts the carbohydrate weight (in grams) for each detected food item.

---

## 🚀 Features

- 🍛 **Food Detection**: Uses a trained YOLOv8 model to detect and classify food items.
- 🔍 **Feature Extraction**: Captures spatial and intensity-based features like area, aspect ratio, and pixel intensity.
- 📦 **Hybrid Model Architecture**: Combines features from both MobileNetV3 image embeddings and geometric statistics for weight prediction.
- 📊 **Ground Truth Mapping**: Associates detected food items with their real carbohydrate weights from a structured dataset.
- 🧪 **End-to-End Pipeline**: From raw image to predicted carbohydrate weight, ready for training or inference.

---

## 🧠 Model Architecture

1. **YOLOv8**:
   - Detects and labels food items.
   - Provides bounding boxes for cropping.

2. **Feature Fusion**:
   - Cropped food images are passed through `MobileNetV3` (pretrained).
   - Additional features extracted:
     - Bounding box **area**
     - **Aspect ratio** (width / height)
     - **Mean pixel intensity**

3. **Weight Estimation Model**:
   - Fully connected network taking both MobileNetV3 embeddings and custom features.
   - Predicts **carbohydrate weight (grams)** as a regression output.

---

## 📂 Repository Structure


