### Transforming Data: Baxkground
- Models used in Machine LEarnig  Workflows often make assumptions about the data

### Transforming Data: Distributions 
- Predictions from Linear Regression models assume residuals are normally distributed.
- Features and predicted data are often skewed(distorted away from the center).
- Skewness refers to the measure of asymmetry in a distribution.

- ##### usdeful transform functions
    - from numpy import lg , log1p
    - from scipy.stats import boxcox

- ##### Polynomial Features: Syntax
    - 1.) Import Class containing the transformation method
        - from sklearn.preprocessing import PloynomialFeatures
    - 2.) Create an instance of the class (choose the no.degrees)
        - polyFeat = PolynomialFeatures(degree=2)
    - 3.) Create the polynomial features and then transform the data
        - polyFeat = polyFeat.fit(X_data)
        - X_poly = polyFeat.transform(X_data)

### Variable Selection: Background 
- It means choosing the set of features to include in the model 
- Variables must often be transformed before they can be included in models.
    - Using Log and polynomial transformations
    - Encoding:- Converting non-numeric to numeric features
    - Scaling:- Converting the scale of numeric data so they are on comparable scale

- Encoding is applied to <u>Categorical Data(features)</u> .

    - Binary Encoding: Converts variables to either 0 or 1 and is suitable for variables with True or False values.

    - One-hot encoding: convert variables that take multiple values into binary (0,1) variables,one for each category,creating several ne variable.
        - Eg.: let there be one color column that is "Red, Green,Blue" , we will seperate that one column into three different columns and for each column we will mark a 'True' or  'False' , for being red we will mark 'True' in 'Red' column and if not then 'False'.
        
    - Ordinal Encoding: Involves converting  ordered categories to numeraical values.

### Feature Scaling: Background
- Feature Scaling involves adjusting a variable's scale, which allows comparison of variabes with differenct scales.

- Common Approches:-
    - Standard Scaling: Converts features to standard normal variables(by subtracting the mean and dividing by the standard error)

    - Min-max scaling:-
        - Converts variables to continuous variables in the (0,1) inteval by mapping min values to 0 and max values to 1. This scaling is sensitive to outliers.
        It sutracts the min value from that specific column and divides by (max-min)

    - Robust Scaling:-
        - It is similar to min-max scaling , but instead maps the interquartile range(75%-25%) to (0,1).
        - This allows avoid any skew from the outliers 




     

