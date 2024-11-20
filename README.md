Predict Used Car Price
=======================

# Business Objective 

Develop a model to accurately predict prices of used cars. This way my client, a used car dealership, can set the competitive price for their inventory.


# Business Success Criteria 



* Minimize the difference between predicted car price and actual prices.
* Figure Out which factor has the most influence on determining used car  prices. 


# Data Understanding 

This step includes looking at the existing data, missing values, splitting the data in training and test then imputing the values before training the model.


## Collect Initial Data

A dataset from Kaggle is used for predicting used car prices. This dataset contains 426K cars. Load the csv data to dataframe. 


```
df = pd.read_csv('/content/drive/MyDrive/Berkeley/module_11/vehicles.csv')
df.info()
```


A quick overview of data:


```
RangeIndex: 426880 entries, 0 to 426879
Data columns (total 18 columns):
 #   Column        Non-Null Count   Dtype  
---  ------        --------------   -----  
 0   id            426880 non-null  int64  
 1   region        426880 non-null  object 
 2   price         426880 non-null  int64  
 3   year          425675 non-null  float64
 4   manufacturer  409234 non-null  object 
 5   model         421603 non-null  object 
 6   condition     252776 non-null  object 
 7   cylinders     249202 non-null  object 
 8   fuel          423867 non-null  object 
 9   odometer      422480 non-null  float64
 10  title_status  418638 non-null  object 
 11  transmission  424324 non-null  object 
 12  VIN           265838 non-null  object 
 13  drive         296313 non-null  object 
 14  size          120519 non-null  object 
 15  type          334022 non-null  object 
 16  paint_color   296677 non-null  object 
 17  state         426880 non-null  object 
```



## Split Data

Let’s split the data first then we will impute the missing values.
