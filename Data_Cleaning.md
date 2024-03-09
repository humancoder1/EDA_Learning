- observations: An instance of data(point or row in dataset)
- Labels: Output variables being predicted 
- Algorithms: Computer programs that estimate models based on avilable data
- Impute: is a common term referring to different statistical tools that can be used to calculate missing values from your dataset.
- Hyperparameters: are settings on the model that are not changed during training, but can affect how quickly or how reliably the model trains, such as the number of clusters the model should identify.

### Model Training
- Training dataset: The data on which the model will be trained. Most of your data will be here. Many developers estimate about 80%.
- Test dataset: The data withheld from the model during training, which is used to test how well your model will generalize to new data.

##### Messy Data:-
- Duplicate or unnecessary Data
- Inconsistent text and typos
- Missing data
- Outliers
- Data Sourcing issues:
    - Multitple systems 


##### Policies for Missing Data
- Remove the data : Remove the row completely
    - disadvantage is if certain columns is missing values for many rows , removing data may end up losing too much data
- Impute the data : replace with substituted values. 
    - merit-> we don't lose full rows and data
    - demerit -> we add another uncertainty to the model because it is trained on estimated values.
- Mask the data : create a category for missing values.
    - merit-> we don't lose full rows and data
    - demerit -> we add another uncertainty to the model because it is based on the assumption that all missing values are alike.


##### Outliers
- It is an observation in the data that is disant form most other observations.
- to find outliers we can use :-
    - Boxplots
    - Histograms

##### Residuals
- It is the difference between actual and predicted values of the outcome variables.
- It represents model failure.
- How to Calculate Residuals:-
    - Standardized : residual divided by standard error.
    - Deleted : residual from fitting model on all data excluding current observation.
    - Studentized : Deleted residuals divided by residual standard error.(It is just taking the deleted residuals and standardized them )

##### After detecting Outliers :
- Remove them
    -advantage - no need to worry about the outliers effects
    -disadvantage - the entire row related to the outlier value will get lost

- Assign new value : mean or median
    - disadvantage : lossing the important value

- Transform : we can tranform the column that had the outlier

- Predict :
    - By using similar observations
    - By using Regression

- Keep the outliers


