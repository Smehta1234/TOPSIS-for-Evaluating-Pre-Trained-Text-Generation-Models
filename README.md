# TOPSIS for Evaluating Pre-Trained Text Generation Models

This repository demonstrates how to use the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method to rank pre-trained text generation models based on various performance criteria.

## Features
- Prepares and evaluates a list of popular pre-trained models for text generation (e.g., GPT-3, T5, BLOOM, etc.).
- Ranks models using the TOPSIS method with weighted evaluation criteria.
- Provides input and output files for demonstration.
- Visualizes results through graphs and tables for easy understanding.

## Repository Contents

### `models_metrics.csv`
Input file containing performance metrics of pre-trained models (e.g., perplexity, BLEU score, inference time, etc.).

### `results.csv`
Output file showing the rankings of models based on the TOPSIS method.

### `generate_csv.py`
Script to dynamically generate the input CSV file with model metrics.

### Python TOPSIS Package
Custom Python package for applying the TOPSIS method to the input data.

### `README.md`
Instructions for running the TOPSIS analysis and understanding the results.

## How to Use

### Clone the Repository
```bash
git clone https://github.com/your_username/topsis-text-generation.git
cd topsis-text-generation
```

### Generate or Edit the Input CSV File
- Use the provided `generate_csv.py` script to create the file:
  ```bash
  python generate_csv.py
  ```
- Alternatively, manually edit the `models_metrics.csv` file with your data.

### Run the TOPSIS Analysis
```bash
python -m my_topsis_package.__main__ models_metrics.csv "1,1,1,1,1" "+,+,-,+,+" results.csv
```
- The weight vector (`1,1,1,1,1`) specifies the relative importance of each criterion.
- The signs (`+,+,-,+,+`) indicate whether higher values are better (`+`) or lower values are better (`-`).

### View Results
The results will be saved in `results.csv`. You can open it to see the rankings of the models.

## Evaluation Criteria
The models are evaluated based on the following criteria:
1. **Perplexity**: Measures the model's ability to predict text (lower is better).
2. **BLEU Score**: Measures text similarity to reference outputs (higher is better).
3. **Inference Time**: Time taken to generate a response (lower is better).
4. **Model Size**: Storage size of the model (higher size may imply more complexity).
5. **Training Data Size**: Amount of data used to train the model (higher is better).

## Dependencies
- Python 3.6+
- CSV support (e.g., Pandas or built-in `csv` module)
- Your custom TOPSIS package

## License
This repository is licensed under the MIT License. See the `LICENSE` file for details.


