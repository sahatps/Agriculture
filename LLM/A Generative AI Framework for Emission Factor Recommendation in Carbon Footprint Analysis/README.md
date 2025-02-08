# A Generative AI Framework for Emission Factor Recommendation in Carbon Footprint Analysis

   This project demonstrates a carbon footprint calculation tool implemented that uses a zero‑shot classification model to automatically assign an emission factor (EF) based on product descriptions. The tool then combines these EF values with corresponding cost data to compute the total carbon emissions for each product, offering an automated, reproducible, and transparent method for environmental impact assessment.

---

## Colab Notebook

Access the interactive Colab notebook to run and experiment with the project code:

[https://colab.research.google.com/drive/1vNP1-xIaJYXdwemNvQaWWAJNaHiKNZvf#scrollTo=ZWYwTqnIxJje](https://colab.research.google.com/drive/1vNP1-xIaJYXdwemNvQaWWAJNaHiKNZvf#scrollTo=ZWYwTqnIxJje)

---

## Project Overview

This project leverages a zero‑shot classification model from Hugging Face to analyze unstructured product descriptions and automatically recommend an appropriate emission factor (EF). By integrating cost or activity data with the predicted EF, the system calculates the total carbon footprint (in kg CO₂e) for each product. The approach is designed to automate and standardize the carbon footprint calculation process, thereby reducing manual workload and improving the reproducibility and transparency of environmental assessments.

---

## Input, Output, Objective, and Limitations

1. **Input:**
   - Unstructured product descriptions.
   - Associated cost or activity data for each product.

2. **Output:**
   - Predicted emission factor (EF) labels along with confidence scores.
   - Computed total carbon emissions (e.g., in kg CO₂e) for each product.

3. **Objective:**
   - To automate the process of recommending emission factors using a generative AI framework.
   - To calculate the carbon footprint of products accurately and transparently by integrating EF values with cost data.
   - To provide an automated and reproducible method for environmental impact assessment.

4. **Limitation:**
   - Dependence on the quality and clarity of the input product descriptions.
   - The EF mappings are based on simulated or limited data and require further validation against authoritative databases.
   - The pre-trained zero‑shot classification model may not fully capture all industry-specific terminologies or contexts.
   - Scalability may be challenged when extending to a diverse range of product categories without additional fine‑tuning.

---

## How to Use

1. **Installation:**  
   Open the Colab notebook and run the first cell to install the necessary dependencies (e.g., the Hugging Face Transformers library).

2. **Import Libraries and Data:**  
   Subsequent cells import required libraries and load the sample product data into a DataFrame.

3. **Model Initialization:**  
   The notebook initializes a zero‑shot classification model to predict EF labels based on product descriptions.

4. **Processing and Calculation:**  
   The model is applied to each product description to generate predicted EF values and scores. These predictions are then combined with cost data to compute the total carbon emissions.

5. **Experimentation:**  
   Users can modify the sample inputs, adjust candidate EF labels, or update the cost data to see how the output changes.

---

## Contributing

Contributions and suggestions for improvements are welcome! Feel free to open issues or submit pull requests to enhance this project.

---

## License

This project is licensed under the terms of the MIT License. See the [LICENSE](LICENSE) file for details.
