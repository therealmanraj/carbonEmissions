# carbonEmissions

---

## Objective
The goal of this project is to build a predictive linear regression model for estimating a car’s CO2 emissions (grams/km). The dataset is sourced from the Government of Canada's "Fuel Consumption Ratings."

---

## Project Highlights
1. Performed descriptive analysis to determine significant features.
2. Divided the dataset into 80% training and 20% testing subsets.
3. Explored multiple models:
    - **"Enhanced Interaction Model" (Model 8):** High accuracy and eliminated residual patterns using interactions.
    - **"Simplified Efficiency Model" (Model 9):** Compact, interpretable, and effective.
4. Compared the performance of chosen models using RMSE and predictive power on testing data.

---

## Modeling Process

### Descriptive Analysis
- Significant correlations identified:
    - CO2 Emissions vs Fuel Consumption: **0.935**
    - CO2 Emissions vs Engine Size: **0.799**
- High correlations between predictors informed decisions on feature selection and interaction terms.

### Key Insights
- **Fuel Type:** Ethanol and Natural Gas showed the highest CO2 emissions.
- **Transmission Type:** Continuous Variable Transmission (CVT) had the lowest emissions.
- **Vehicle Class:** Dropped due to lack of predictive clarity after unification efforts.

---

### Final Models

#### **Enhanced Interaction Model (Model 8)**
**Formula:**  
`CO2 Emissions ~ Fuel Consumption + Fuel Type + Year + Gears + Transmission + Engine Size + Fuel Consumption*Fuel Type`

- R-squared: **0.9992**
- RMSE: **1.83**
- Benefits:
  - Incorporates an interaction term to improve predictive accuracy.
  - Suitable for comprehensive analysis.

#### **Simplified Efficiency Model (Model 9)**
**Formula:**  
`CO2 Emissions ~ Fuel Consumption + Fuel Type + Fuel Consumption*Fuel Type`

- R-squared: **0.9985**
- RMSE: **2.47**
- Benefits:
  - Compact and interpretable with only three coefficients.
  - Chosen for its simplicity and robust performance.

---

## Testing Results
Both models performed similarly on the testing dataset, with Model 9 offering slightly reduced complexity while maintaining high predictive accuracy.

---

## Conclusions
Model 9 was selected as the final model due to its:
1. **Simplicity:** Minimal predictors without sacrificing performance.
2. **Accuracy:** High adjusted R-squared (0.9985) with reasonable RMSE.
3. **Efficiency:** Excellent balance between interpretability and predictive power.

---

## Acknowledgments
Special thanks to the team members for their contributions to the analysis and modeling efforts.
