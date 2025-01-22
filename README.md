# Wine Quality - Fitting a Statistical Model
**June 2024**<br>
**Celine Ng**<br>

## Project Description
This project aims to analyze the [Red Wine Quality](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009) <br>
dataset from kaggle, understanding and identifying factors that influence 
wine <br> quality. <br><br>

**Data**
The dataset includes 12 columns. 11 are input variables, features that help 
<br> describe the wine. 1 is the output variable, where the wine receives a<br>
score from 0 to 10.

## Approach & Methodology
Identify which variable influences perceived wine quality the most by<br>
fitting a statistical model, with an explanatory model approach. For this 
project, I approached this problem by following a structured methodology of data exploration, preprocessing, and modeling.
1. Data Exploration: As linear models were to be used in this project, it 
   is essential to understand the data distribution, correlation, and 
   multicollinearity.
2. Preprocessing: Split data into train/test sets, and scale features.
3. Modeling: Applied Ordinal Logistic Regression due to the nature of 
   target variable, and access model with pseudo r-squared and residuals.

## Results
Alcohol has the largest impact on the dependent variable, with a coefficient
 <br>
 of 0.97. So replying to the initial hypothesis, alcohol is the most <br>
influential factor for red wine quality.
Looking into r-squared value, only 18% of the dependent variable is 
explained by our model (independent variables), meaning our model does not 
capture the relationships well.

## Challenges & Learnings
Residuals were scattered around 3 and not 0. As the distribution seems 
normal, the problem is due to a missing constant. This 
problem could have arisen 
from the target variable in reality only ranging between 3-8, and not 0-10 
as intended. So the model assumed 3, the lowest label, as 0, and so 
on. In the next iteration, r-squared value is expected to improve significantly
after this correction.