# 🔥 Post-Fire Burn Severity Analysis & Burn Scar Detection using Sentinel-2 and Google Earth Engine 🔥

This project identifies and classifies **burn severity** in a specified region using **Sentinel-2 satellite imagery** and **Google Earth Engine (GEE)**. The analysis focuses on detecting **burn scars** and measuring fire impact by comparing pre-fire and post-fire conditions. The results are visualized interactively using **Geemap**.

> 🚀 Try the Colab Notebook here: [Post-Fire Burn Severity Analysis & Burn Scar Detection using Sentinel-2 and Google Earth Engine](https://colab.research.google.com/drive/1pZx0-gO2oZHFxuCFLZ4hOJsRlnpNMWTC)

![Image](https://github.com/user-attachments/assets/80124741-72b6-459d-a9c1-2706c5ff50cc)

## 🌟 **Key Features**
- **Pre-Fire vs. Post-Fire Analysis:** Analyze and compare satellite images from before and after the fire event.
- **Burn Severity Classification:** Compute the **Differenced Normalized Burn Ratio (dNBR)** and classify areas into burn severity categories.
- **Cloud Masking:** Automatically remove cloud-covered pixels using Sentinel-2’s **QA60 band**.
- **Interactive Map Display:** Visualize burn severity and detected burn scars on an interactive map.

---

## 🛠️ **Tech Stack**
- **Google Earth Engine (ee):** For retrieving and processing Sentinel-2 satellite imagery.
- **Geemap:** For interactive visualization of geospatial data.
- **Google Colab:** For running the analysis in a Python environment.

---

## ⚙️ **How It Works**
1. **Authentication and Initialization:**
   - Authenticate with Google Earth Engine using Colab’s built-in methods and initialize the project.

2. **Area of Interest (AOI):**
   - The region to be analyzed is defined using a polygon boundary.

3. **Cloud Masking Function:**
   - The QA60 band from Sentinel-2 is used to mask clouds and cirrus for more accurate analysis.

4. **Pre-Fire and Post-Fire Image Collections:**
   - Pre-fire images are collected from **December 2021 to January 2022**.
   - Post-fire images are collected from **January 2022 to February 2022**.
   - Median composites are generated after filtering for cloud cover (<20%).

5. **Calculating dNBR (Differenced Normalized Burn Ratio):**
   - **Normalized Burn Ratio (NBR)** is calculated using Sentinel-2 bands:
     - Band 8 (Near Infrared - NIR)
     - Band 12 (Shortwave Infrared - SWIR)
   - The dNBR is computed as the difference between pre-fire and post-fire NBR values to measure fire impact.

6. **Burn Severity Classification:**
   - Threshold-based classification is applied to identify regions of severe, moderate, and low/no burn.

7. **Visualization:**
   - An interactive map is displayed using **Geemap** with color-coded layers:
     - **dNBR Layer:** Shows the burn severity (blue to red scale).
     - **Burn Scar Mask:** Highlights burn-affected areas.

---

## 🔧 **Getting Started**

### 1. Open the Colab Notebook
- Click the link to open the notebook: [Post-Fire Burn Severity Analysis](https://colab.research.google.com/drive/1pZx0-gO2oZHFxuCFLZ4hOJsRlnpNMWTC)

### 2. Authenticate and Run the Notebook
- Follow the instructions in the notebook to authenticate your Google Earth Engine account.
- Run all cells to perform the burn severity analysis.

---

## 📊 **Visualization Layers**
- **dNBR (Differenced Normalized Burn Ratio):**  
  A color-coded representation of fire impact with the following scale:
  - **Severe Burn (Red):** High damage to vegetation
  - **Moderate Burn (White):** Moderate damage
  - **Low/No Burn (Blue):** Minimal to no damage

- **Burn Scar Mask:**  
  Burn scars are highlighted in black, showing areas with significant damage.

---

## 📚 **Resources and References**
- **Google Earth Engine Documentation:** [https://developers.google.com/earth-engine](https://developers.google.com/earth-engine)
- **Sentinel-2 Mission Overview:** [https://sentinels.copernicus.eu](https://sentinels.copernicus.eu)
- **Geemap Documentation:** [https://geemap.org](https://geemap.org)

---

## 📩 **Contact**
For questions or suggestions, please reach out to:  
📧 your-email@example.com

---

## 📜 **License**
This project is licensed under the [MIT License](LICENSE).

