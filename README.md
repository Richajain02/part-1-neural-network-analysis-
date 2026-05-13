# Neural Network Customer Churn Prediction

## Data Source Link

'customer_churn_nn.csv'

## Project Overview

This project builds a feed-forward neural network to predict customer churn.

Target variable:

- churn = 1 → Customer churned
- churn = 0 → Customer retained

The objective is to classify whether a customer is likely to churn based on service usage, payment behavior, satisfaction score, and other customer features.

---

## Dataset Information

Dataset size:

- Rows: 2000
- Columns: 15

Feature types:

### Categorical Features
- region
- plan_type
- contract_type
- payment_method

### Numerical Features
- tenure
- monthly_charges
- login_days
- support_tickets
- payment_delays
- data_usage
- satisfaction_score
- complaint_recency
- discounts_used
- referrals

Target variable:

- churn

Identifier removed:

- customer_id

---

## Steps Performed

### 1. Data Exploration
Performed:

- Shape check
- Missing value analysis
- Statistical summary
- Target distribution analysis

### 2. Data Preprocessing
Performed:

- Removed customer_id
- One-hot encoded categorical variables
- Feature scaling
- Train-test split

### 3. Neural Network Building
Built a feed-forward neural network
Architecture:

- Input layer
- Hidden Layer 1 → 16 neurons, ReLU
- Hidden Layer 2 → 8 neurons, ReLU
- Output layer → 1 neuron, Sigmoid

Loss function:

- Binary Crossentropy

Optimizer:

- Adam

---

## Results

### Training Performance

- Accuracy: 98.5%
- Loss: 0.059

### Testing Performance

- Accuracy: 98.25%
- Loss: 0.068

### Confusion Matrix

[[393, 0],
 [7, 0]]

---

## Hyperparameter Experiments

Three experiments were performed by changing:

- Hidden layers
- Number of neurons
- Batch size

Results are available in:

results/model_comparison_table.csv

---

## Observations

Although the model achieved high accuracy, it failed to detect churn customers due to severe class imbalance.

This shows that accuracy alone is not sufficient for imbalanced classification problems.

Potential improvements:

- SMOTE
- Oversampling
- Better class balancing techniques
