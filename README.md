## Data Cleaning
After scraping the data, it was needed to clean it up so that it was usable for our model. The following changes were made and the following variables were created:

*	Parsed numeric data out of salary 
*	Made columns for employer provided salary and hourly wages 
*	Removed rows without salary 
*	Parsed rating out of company text 
*	Made a new column for company state 
*	Added a column for if the job was at the company’s headquarters 
*	Transformed founded date into age of company 
*	Made columns for if different skills were listed in the job description:
    * Python  
    * R  
    * Excel  
    * AWS  
    * Spark 
    * SQL
*	Column for simplified job title and Seniority 
*	Column for description length 

## Model Building 

Transformed the categorical variables into dummy variables. Split the data into train and tests sets with a test size of 20%.   

Tried three different models and evaluated them using Mean Absolute Error. MAE was chosen because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.   

Tried three different models:
*	**Multiple Linear Regression** – Baseline for the model
*	**Lasso Regression** – Because of the sparse data from the many categorical variables, I thought a normalized regression like lasso would be effective.
*	**Random Forest** – Again, with the sparsity associated with the data, I thought that this would be a good fit. 

## Model performance
The Random Forest model far outperformed the other approaches on the test and validation sets. 
*	**Random Forest** : MAE = 11.22
*	**Linear Regression**: MAE = 18.86
*	**Ridge Regression**: MAE = 19.67