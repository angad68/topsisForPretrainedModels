
# TOPSIS-Based Model Selection for Text Summarization

## Introduction
This project applies the **Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS)** to rank and select the best pre-trained model for **Text Summarization** tasks based on multiple evaluation criteria.

## Dataset
The decision matrix includes the following criteria for evaluating four pre-trained models:

| Model       | ROUGE | Inference Time (ms) | Model Size (MB) | F1 Score |
|-------------|-------|---------------------|-----------------|----------|
| BART        | 0.85  | 120                 | 500             | 0.87     |
| T5          | 0.88  | 150                 | 400             | 0.89     |
| Pegasus     | 0.86  | 110                 | 600             | 0.88     |
| DistilBART  | 0.83  | 100                 | 350             | 0.84     |

## Criteria Weights
The assigned weights for the criteria are:

- ROUGE: **0.4** (beneficial)
- Inference Time: **0.2** (non-beneficial)
- Model Size: **0.2** (non-beneficial)
- F1 Score: **0.2** (beneficial)

## Steps to Execute the TOPSIS Method

1. **Data Initialization:** Load and display the dataset.
2. **Normalization:** Normalize each criterion using beneficial and non-beneficial rules.
3. **Weighted Normalization:** Multiply normalized values by the assigned weights.
4. **Ideal Solutions:** Determine the ideal best and worst solutions.
5. **Distance Calculation:** Compute distances to the ideal best and worst solutions.
6. **Closeness Coefficient Calculation:** Calculate the closeness to the ideal solution.
7. **Model Ranking:** Rank models based on their TOPSIS scores.

## Output Example
Final Ranking:

| Model       | TOPSIS Score | Rank |
|-------------|--------------|------|
| T5          | 0.90         | 1    |
| Pegasus     | 0.87         | 2    |
| DistilBART  | 0.85         | 3    |
| BART        | 0.80         | 4    |

## Visualizations

### TOPSIS Score Plot
![TOPSIS Score Plot](path-to-image.png)

### Criteria Distribution Plot
![Criteria Distribution Plot](path-to-criteria-plot.png)

## How to Run the Code

1. Install the required packages:
   ```bash
   pip install numpy pandas matplotlib
   ```

2. Execute the script:
   ```bash
   python topsis_text_summarization.py
   ```

## Conclusion
The TOPSIS method successfully ranks text summarization models based on multiple criteria. The model with the highest closeness coefficient is identified as the best choice.

## License
This project is licensed under the MIT License.

---
Feel free to replace placeholder image paths with your actual image paths and adjust formatting if necessary.
