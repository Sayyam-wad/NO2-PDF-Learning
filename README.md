# Learning Probability Density Function using Non-Linear Transformation on NO2 Data

## Objective
This project implements a non-linear transformation on NO2 concentration values and learns the parameters of a probability density function (PDF) of the transformed variable as part of Assignment-1.

The transformation applied is:

z = x + a_r sin(b_r x)

where:
- a_r = 0.05 × (r mod 7)  
- b_r = 0.3 × (r mod 5 + 1)  
- r is the university roll number.

The learned PDF is:

p̂(z) = c · exp(−λ (z − μ)²)

The parameters λ, μ, and c are estimated from the transformed data.

---

## Dataset
India Air Quality Dataset (NO2 feature used)

Source:  
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

---

## Methodology

1. The NO2 column is extracted from the dataset and cleaned by removing missing values.
2. A roll-number-parameterized non-linear transformation is applied to obtain the transformed variable z.
3. The parameters of the probability density function are estimated:
   - μ as the mean of z
   - λ using variance of z
   - c as the normalization constant
4. The learned PDF is visualized against the histogram of transformed data.

---

## Files in Repository

- `102303147_asgn.ipynb`  
  Contains the complete implementation and results.

---

## Results

The model successfully learns the probability density function of the transformed NO2 data.  
The final values of λ, μ, and c are obtained programmatically and submitted as required.

---

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload the dataset CSV file.
3. Run all cells sequentially to reproduce results.

---

## Author
Assignment submission for coursework.
