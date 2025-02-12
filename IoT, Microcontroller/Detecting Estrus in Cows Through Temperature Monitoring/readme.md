# 🐄 Detecting Estrus in Cows Through Temperature Monitoring 🐄

This project utilizes **temperature-based activity monitoring** to detect estrus (heat) in cows using **Python and Pandas**. The system processes **activity change data** from an uploaded Excel file, applies **data cleaning**, and then detects heat events based on **activity thresholds**.

> 🚀 **Try the live notebook here:** [Open in Colab](https://colab.research.google.com/drive/1yxKlbDP0oc_pGXtvgJt8UiUqhCit8UNH?usp=sharing)
![Image](https://github.com/user-attachments/assets/74ee57bb-4d2c-455c-8ea5-94624854ad0c)
---

## 🌟 **Key Features**
- **Automated Data Processing:**
  - Reads and cleans data from an Excel file.
  - Merges separate **Date** and **Time** columns into a single **Datetime** column.
  - Filters out missing values to ensure clean data.

- **Heat Detection Algorithm:**
  - Identifies heat events based on a predefined **activity change threshold**.
  - Groups consecutive activity peaks into distinct **heat events**.
  - Ensures detected heats are at least **10 hours apart** to avoid false positives.

- **Dynamic Data Filtering:**
  - Users can adjust **heat thresholds**, **minimum duration**, and **cool-down periods** to fine-tune detection.

- **Final Output:**
  - Provides a DataFrame containing detected **heat events**, including:
    - **Start time**  
    - **End time**  
    - **Duration (in hours)**  
    - **Maximum activity change recorded**

---

## 🛠️ **Tech Stack**
- **Google Colab**: Interactive execution environment for Python.  
- **Pandas**: Data processing and analysis.  
- **Itertools**: Grouping consecutive activity peaks for heat detection.  
- **Datetime Handling**: Conversion of timestamps for time-based analysis.  

---

## ⚙️ **How It Works**

### 1️⃣ **Upload the Dataset**
   - The user uploads an **Excel file** containing cow activity data.
   - The script dynamically detects the **file name** and reads the data into a Pandas **DataFrame**.

### 2️⃣ **Data Preprocessing**
   - Combines **Date** and **Time** columns into a **single datetime column**.
   - Filters only the necessary columns:  
     - **Cow Number**
     - **Datetime**
     - **Activity Change**
     - **Lactation Number**
     - **Days in Lactation**
   - Removes **missing values** to ensure accuracy.

### 3️⃣ **Heat Detection Algorithm**
   - Identifies timestamps where **Activity Change** exceeds a **threshold (default = 35)**.
   - Groups consecutive high-activity timestamps into **individual heat events**.
   - Filters out **short heat events** (must last at least **6 hours**).
   - Ensures at least **10 hours gap** between consecutive heats.

### 4️⃣ **Results Generation**
   - Outputs a **DataFrame** of detected heat events with:
     - **Start and End Times**
     - **Duration of Heat Event**
     - **Peak Activity Level**
   - Displays the results in **Google Colab**.

---

## 🔧 **Getting Started**

### Option 1: Run Directly in Google Colab  
1️⃣ **Open the notebook**: [Click here to open](https://colab.research.google.com/drive/1yxKlbDP0oc_pGXtvgJt8UiUqhCit8UNH?usp=sharing)  
2️⃣ **Upload your Excel file** containing cow temperature activity data.  
3️⃣ **Execute each cell** to process and analyze the dataset.  
4️⃣ **View detected heat events** in the final output.

---

## 📊 **Example Output**
| Heat No | Start Time           | End Time             | Duration (hours) | Max Activity |
|---------|----------------------|----------------------|------------------|--------------|
| 1       | 2025-02-12 06:00:00  | 2025-02-12 18:00:00  | 12               | 42           |
| 2       | 2025-02-13 08:00:00  | 2025-02-13 20:00:00  | 12               | 39           |

---

## 📝 **Customization Options**
You can **tweak detection parameters** by modifying:
- **`threshold`** (default `35`): Adjusts the sensitivity of heat detection.
- **`min_heat_duration`** (default `6 hours`): Minimum duration required for a valid heat.
- **`min_hours_between_heats`** (default `10 hours`): Ensures sufficient spacing between heats.

---

## ⚡ **Dependencies**
The project requires the following **Python libraries**:
- `pandas`
- `itertools`
- `datetime`
- `google.colab` (for file uploads)

All required dependencies **are pre-installed in Google Colab**, so no manual installation is needed.

---

## 🤝 **Contributions**
Contributions are **welcome!** 🎉 Feel free to submit issues or suggest improvements.

---

## 📜 **License**
This project is licensed under the **MIT License**.

---
