# 🔥 Burn Scar Detection using Sentinel-2 and Google Earth Engine 🔥

This project analyzes **Sentinel-2 satellite imagery** to detect burn scars after a fire event using **Google Earth Engine (GEE)**. It computes key vegetation and water indices (dNBR, MNDWI, SAVI) and visualizes burn areas on an interactive map.

> 🚀 Run this project in Google Colab: [Burn Scar Detection Colab Notebook](https://colab.research.google.com/drive/1pZx0-gO2oZHFxuCFLZ4hOJsRlnpNMWTC)

---

## 🌟 **Key Features**
- **Burn Scar Detection:** Automatically detects and masks areas affected by fire.
- **Multi-Index Analysis:** Utilizes dNBR (burn severity), MNDWI (water detection), and SAVI (vegetation health) for accuracy.
- **Cloud Masking:** Effectively masks clouds and cirrus using Sentinel-2's QA60 band.
- **Interactive Map:** Visualize burn severity and masked areas on an interactive map using **Geemap**.

---

## 🛠️ **Tech Stack**
- **Google Earth Engine (ee):** For satellite data processing.
- **Geemap:** For displaying map-based outputs.
- **Colab:** For easy, cloud-based execution.

---

## ⚙️ **How It Works**
1. **Authenticate and Initialize GEE:**  
   The project starts by authenticating and initializing the **Google Earth Engine** environment.

2. **Area of Interest Definition:**  
   Defines a geographic region using a bounding box polygon.

3. **Pre- and Post-Fire Image Selection:**  
   Retrieves **Sentinel-2 surface reflectance data** for two periods:  
   - **Pre-Fire:** (2021-12-01 to 2022-01-15)  
   - **Post-Fire:** (2022-01-16 to 2022-02-28)  

4. **Cloud Masking:**  
   Applies a cloud and cirrus mask using the **QA60 quality band** to minimize errors in detection.

5. **Index Calculation:**  
   The following indices are computed:
   - **dNBR (Differenced Normalized Burn Ratio):** Identifies burn severity by comparing pre- and post-fire conditions.
   - **MNDWI (Modified Normalized Difference Water Index):** Masks water bodies to avoid false positives.
   - **SAVI (Soil Adjusted Vegetation Index):** Reduces soil interference in vegetation analysis.

6. **Burn Scar Masking:**  
   Combines thresholds of dNBR, MNDWI, and SAVI to create a burn scar mask.

7. **Visualization:**  
   Displays the results on an interactive map using **Geemap**, with two main layers:  
   - **dNBR Map:** Color-coded based on burn severity  
   - **Final Burn Scar Mask:** Highlighted in black  

---

## 🔧 **Getting Started**

### 1. Open in Google Colab
Click here to open and run the project in Colab: [Burn Scar Detection Colab](https://colab.research.google.com/drive/1pZx0-gO2oZHFxuCFLZ4hOJsRlnpNMWTC)

### 2. Install Required Libraries
Ensure you have the necessary libraries by running:
```python
!pip install geemap earthengine-api
