# 🌍 Comparing Machine Learning Classifiers for Land Cover Mapping in Google Earth Engine 🌍

This is a **web-based application** that compares various machine learning classifiers for **land cover classification** using **Sentinel-2 satellite imagery**. The application is built using **Google Earth Engine (GEE)** for satellite data processing and **Colab** for interactive execution.

> 🚀 **Try the live notebook here:** [Open in Colab](https://colab.research.google.com/drive/1DM5DY2cs2x-NTMmzPcAKDmrjjcp8urkO)

---

## 🌟 **Key Features**
- **Classifier Comparison:** Evaluate six machine learning models on land cover classification:
  - Minimum Distance  
  - K-Nearest Neighbor (KNN)  
  - Support Vector Machine (SVM)  
  - Decision Trees (CART)  
  - Random Forest  
  - Gradient Tree Boosting  
- **Hyperparameter Tuning:** Automatically search for the best Random Forest model using grid search.
- **Accuracy Assessment:** Compute metrics such as overall accuracy, user accuracy, producer accuracy, and confusion matrices.
- **Interactive Map Visualization:** Display classified outputs and Sentinel-2 imagery using **geemap**.

---

## 🛠️ **Tech Stack**
- **Colab:** For running Python code interactively in the cloud.
- **Google Earth Engine (ee):** For satellite data acquisition and processing.
- **Geemap:** For interactive visualization of land cover classifications.

---

## ⚙️ **How It Works**

### 1. **Authentication with Google Earth Engine:**  
   The notebook uses the **Earth Engine Python API**. Users authenticate using their Google account.

### 2. **Sentinel-2 Image Processing:**  
   Sentinel-2 imagery is filtered based on cloud cover (<20%) and date range. Cloud masking is applied using the **QA60 band**, and a **median composite** is generated for the study area.

### 3. **Training Data Preparation:**  
   Training polygons representing various land cover classes are sampled. Data is split into **70% training** and **30% testing** sets.

### 4. **Classifier Training and Evaluation:**  
   Six machine learning models are trained using the **training data** and evaluated using the **testing data**:
   - Minimum Distance  
   - KNN  
   - SVM  
   - CART  
   - Random Forest  
   - Gradient Tree Boost  

   For each model, metrics such as overall accuracy, user accuracy, producer accuracy, and error matrices are computed.

### 5. **Hyperparameter Tuning (Random Forest):**  
   The script uses grid search to find the best combination of parameters for the Random Forest classifier:
   - Number of trees  
   - Variables per split  
   - Minimum leaf population  

   The best model is identified based on overall accuracy.

### 6. **Interactive Visualization:**  
   The classified outputs of each model are visualized on an **interactive map**, with different land cover classes represented by color-coded layers.

---

## 🔧 **Getting Started**

### Option 1: Run Directly in Colab  
1. **Open the notebook**: [Click here to open](https://colab.research.google.com/drive/1DM5DY2cs2x-NTMmzPcAKDmrjjcp8urkO)  
2. **Follow the instructions** for authentication and execute each cell sequentially.

---

## ⚙️ **Key Outputs**
- **Classifier Performance Metrics:**  
  - Error matrices  
  - Overall accuracy  
  - User accuracy  
  - Producer accuracy  

- **Interactive Maps:**  
  - Sentinel-2 imagery  
  - Land cover classifications for each model  

---



---

## 📝 **Customization Options**
You can customize this project by:
- Modifying the **study area boundary** to analyze different regions.
- Adding new classifiers or tuning hyperparameters to improve accuracy.
- Changing the date range to analyze time-specific imagery.

---

## ⚡ **Dependencies**
The project requires the following Python libraries (included in Colab):
- `earthengine-api`
- `geemap`
- `pandas`
- `matplotlib`
- `numpy`

---

## 🤝 **Contributions**
Contributions are welcome! Feel free to submit pull requests or raise issues on GitHub to suggest improvements.

---



---

## 📜 **License**
This project is licensed under the **MIT License**.
