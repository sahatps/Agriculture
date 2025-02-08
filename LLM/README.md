# Parakeet: A Generative AI Framework for Emission Factor Recommendation in Carbon Footprint Analysis

## Overview
Parakeet is an AI-driven framework designed to automate the calculation of a product’s carbon footprint by leveraging advanced natural language processing and life cycle assessment (LCA) methodologies. The system processes unstructured product descriptions, uses a zero-shot classification model to recommend appropriate emission factors (EF), and computes the overall greenhouse gas emissions based on associated cost or activity data. This integration streamlines sustainability reporting, reduces manual effort, and enhances the transparency and accuracy of environmental impact assessments.

## Features
- **Automated EF Recommendation:**  
  Uses a pre-trained zero-shot classification model (e.g., Facebook BART-large-MNLI) to match product descriptions with candidate emission factor values.
  
- **Carbon Footprint Calculation:**  
  Computes total carbon emissions (in kg CO₂e) by multiplying the cost (or activity data) by the predicted emission factor.
  
- **Modular and Readable Code:**  
  The code is organized into clear sections in a Google Colab notebook, making it easy to follow, modify, and extend.
  
- **Interactive Demonstration:**  
  The project is implemented in Google Colab, enabling interactive experimentation and real-time visualization of results.

## Input and Output
1. **Input:**  
   - Unstructured product descriptions (e.g., "A high density polyethylene bag used for packaging food items.")  
   - Associated cost or activity data (e.g., cost in USD)
   
2. **Output:**  
   - Predicted emission factor (EF) labels with confidence scores  
   - Computed total carbon emissions (e.g., in kg CO₂e)

## Objective
- **Objective:**  
  To automate the process of assigning emission factors and calculating carbon footprints using generative AI, thereby accelerating sustainability reporting and supporting data-driven decision-making for reducing environmental impact.

## Limitations
- Dependence on the quality and clarity of input product descriptions.
- EF mappings are currently based on simulated or limited data and may require validation against authoritative databases.
- The pre-trained zero-shot model might not capture all industry-specific terminologies without further fine-tuning.
- Scaling the approach for diverse product categories could necessitate additional customization.

## Usage
1. Open the project in Google Colab using the following link:  
   [Parakeet Colab Notebook](https://colab.research.google.com/drive/1vNP1-xIaJYXdwemNvQaWWAJNaHiKNZvf#scrollTo=ZWYwTqnIxJje)
   
2. Run the notebook cells sequentially. The notebook is divided into the following sections:
   - **Section 1: Installation of Dependencies**  
     Installs the Hugging Face Transformers library.
   - **Section 2: Import Required Libraries**  
     Imports pandas and the zero-shot classification pipeline.
   - **Section 3: Create Extended Sample Input Data**  
     Creates a DataFrame with sample product data and descriptions.
   - **Section 4: Set Up the Zero-Shot Classification Model**  
     Initializes the model and defines candidate emission factor labels.
   - **Section 5: Define a Function to Get the Emission Factor**  
     Implements a function that uses the model to predict EF based on product descriptions.
   - **Section 6: Apply the Function to the Data**  
     Applies the function to the DataFrame to generate EF predictions and scores.
   - **Section 7: Add Cost Data and Map EF Values**  
     Adds example cost data and maps EF labels to numeric values.
   - **Section 8: Calculate the Carbon Footprint**  
     Computes the total carbon emissions for each product.

## Getting Started
To get started with this project:
- Click on the Colab notebook link above.
- Follow the step-by-step instructions provided in each section.
- Experiment with different input data or modify candidate labels and mappings to fit specific use cases.

## Contributing
Contributions are welcome! Please feel free to open issues or submit pull requests for improvements, additional features, or bug fixes.

## License
This project is licensed under the MIT License.

## Acknowledgements
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- Inspiration from current research in AI-driven carbon footprint analysis.


