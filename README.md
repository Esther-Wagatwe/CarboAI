```markdown
# 🥗 CarboAI: AI-Powered Carbohydrate Estimation from Food Images  

**CarboAI** is an AI-driven system developed to automatically estimate the **carbohydrate content** of meals using food images. This project integrates **YOLOv11 for object detection** and a **Vision Transformer (ViT)** model for carbohydrate estimation, providing a complete pipeline from image capture to nutritional analysis. The system aims to support **dietary monitoring and self-management** for individuals with **Type 2 diabetes**, enabling users to make informed dietary choices through an accessible and automated approach.  

---

## 🚀 Key Features  

- 🍽️ **Food Detection with YOLOv11** — Detects and classifies multiple food items on a plate with high accuracy (98.65%).  
- 📊 **Carbohydrate Prediction with ViT** — Estimates carbohydrate content in grams with a low Mean Absolute Error (MAE) of 3.10 g using the food-to-plate ratio feature.  
- 🧩 **Feature Engineering** — Incorporates geometric and visual features such as food area, aspect ratio, and mean pixel intensity for improved model performance.  
- ⚙️ **Food-to-Plate Ratio** — Uses **edge detection** and **contouring** to segment the plate and compute relative food size, reducing sensitivity to camera distance and image scale.  
- 🧪 **Data Preprocessing** — Handles dataset skewness through log transformation and feature normalization, improving training stability and accuracy.  
- 💡 **Integrated Application** — The trained models are deployed in a user-friendly web application that allows users to upload meal photos and instantly receive carbohydrate estimates.  

---

## 🧠 Model Development  

1. **Object Detection Stage (YOLOv11)**  
   - Detects and localizes food items with near-human precision.  
   - Data augmentation was applied to enhance robustness across varying lighting, angles, and backgrounds.  
   - The model achieved **98.65% prediction accuracy**, proving suitable for real-time use in mobile or web applications.  

2. **Carbohydrate Estimation Stage (ViT)**  
   - Predicts carbohydrate content from cropped food images and extracted features.  
   - Compared multiple architectures (ViT, EfficientNet, MobileNetV3, ResNet18, XGBoost), with ViT performing best.  
   - Incorporation of the **food-to-plate ratio** improved accuracy and generalization, achieving an **MAE of 3.10 g** and **R² = 0.85**.  
   - Smooth L1 and Huber Loss functions were used to ensure stable learning and minimize outlier influence.  

---

## 🔬 Technical Highlights  

- **Programming Language:** Python  
- **Frameworks:** PyTorch, OpenCV, Ultralytics YOLO  
- **Model Evaluation Metrics:** MAE, RMSE, R²  
- **Data Augmentation:** Applied random rotation, brightness adjustment, and flipping for better generalization.  
- **Visualization:** Edge detection and plate mask generation to compute the food-to-plate ratio.  

---

## 💻 Application Integration  

The trained YOLOv11 and ViT models were integrated into a functional web application that enables users to upload food images and receive immediate carbohydrate estimates. This integration bridges AI research with real-world usability, empowering individuals to track their diets and manage Type 2 diabetes effectively.  

---

## ⚖️ Limitations  

The study faced challenges such as dataset imbalance and skewed carbohydrate distributions, which led to underrepresentation of high-carb meals. The use of **2D images** also limited depth perception and volume estimation. Future work will explore incorporating **reference objects** (e.g., spoons or coins) for scale calibration and **semantic segmentation** for more precise boundary detection.  

---

## 🌍 Impact and Future Work  

CarboAI demonstrates the potential of **AI in personalized nutrition** and **diabetes management** within African contexts. By accurately estimating carbohydrate content from culturally relevant foods such as **ugali, chapati, matoke, and sukuma wiki**, this project promotes inclusivity and local relevance in AI applications. Future improvements will focus on expanding datasets, enhancing model fairness, and integrating additional nutrient estimation (protein, fat, and calories).  
