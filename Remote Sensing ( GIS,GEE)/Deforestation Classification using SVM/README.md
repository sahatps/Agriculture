# 🌳 Deforestation Classification using SVM with Google Earth Engine 🌳

This is a **web-based application** designed to classify forested and deforested areas using **Landsat 8 satellite imagery** and a **Support Vector Machine (SVM) classifier**. The application utilizes **Google Earth Engine (GEE)** to retrieve and process satellite imagery and is built using **Streamlit** for the user interface. 

> 🚀 Try the live app here: [Deforestation Classification on Hugging Face](https://huggingface.co/spaces/thprs/Deforestation_Classification_using_SVM)

![Image](https://github.com/user-attachments/assets/81638ab1-d01a-47f3-ac19-04c8d2da0e81)

## 🌟 **Key Features**
- **Interactive Web Interface:** Easily configure and run the classification via the browser.
- **Deforestation Mapping:** Identify forested and non-forested regions using an SVM model.
- **Customizable Parameters:** Users can define the date range for satellite imagery and tune the SVM hyperparameters (`gamma` and `cost`).
- **Visualization:** Interactive map display of classification results, including satellite imagery and training polygons.

---

## 🛠️ **Tech Stack**
- **Streamlit:** For the interactive web interface.
- **Google Earth Engine (ee):** For satellite imagery retrieval and processing.
- **Geemap:** For displaying map-based outputs.
- **Hugging Face Spaces:** Hosting the web application.

---

## ⚙️ **How It Works**
1. **Authentication with Google Earth Engine:**  
   Users must authenticate using a service account or token to access GEE resources.
   
2. **Deforestation Classification:**  
   The app fetches **Landsat 8 satellite imagery** based on the selected date range and location.  
   It uses **hand-drawn polygons** (representing forested and non-forested areas) as the training dataset.

3. **Support Vector Machine (SVM) Classification:**  
   An SVM model is trained with the selected hyperparameters (`gamma` and `cost`).  
   The trained model is applied to classify the satellite image into two classes:
   - **Class 1:** Forest (Green)
   - **Class 0:** Non-Forest / Deforested areas (Red)

4. **Interactive Map Display:**  
   The results are displayed on a map with three layers:
   - **Original Satellite Image (RGB composite)**
   - **Training Polygons**
   - **Classified Image showing forest and deforestation regions**

---

## 🔧 **Getting Started**

### 1. Clone the repository
```bash
git clone https://github.com/your-username/deforestation-classification.git
cd deforestation-classification
