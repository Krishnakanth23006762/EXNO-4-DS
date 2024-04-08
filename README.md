# EXNO:4-DS
# AIM:
To read the given data and perform Feature Scaling and Feature Selection process and save the
data to a file.

# ALGORITHM:
STEP 1:Read the given Data.
STEP 2:Clean the Data Set using Data Cleaning Process.
STEP 3:Apply Feature Scaling for the feature in the data set.
STEP 4:Apply Feature Selection for the feature in the data set.
STEP 5:Save the data to the file.

# FEATURE SCALING:
1. Standard Scaler: It is also called Z-score normalization. It calculates the z-score of each value and replaces the value with the calculated Z-score. The features are then rescaled with x̄ =0 and σ=1
2. MinMaxScaler: It is also referred to as Normalization. The features are scaled between 0 and 1. Here, the mean value remains same as in Standardization, that is,0.
3. Maximum absolute scaling: Maximum absolute scaling scales the data to its maximum value; that is,it divides every observation by the maximum value of the variable.The result of the preceding transformation is a distribution in which the values vary approximately within the range of -1 to 1.
4. RobustScaler: RobustScaler transforms the feature vector by subtracting the median and then dividing by the interquartile range (75% value — 25% value).

# FEATURE SELECTION:
Feature selection is to find the best set of features that allows one to build useful models. Selecting the best features helps the model to perform well.
The feature selection techniques used are:
1.Filter Method
2.Wrapper Method
3.Embedded Method

# CODING AND OUTPUT:
      ```
      import pandas as pd
      from scipy import stats
      import numpy as np
      ```
      ```
      df=pd.read_csv("/content/bmi.csv")
      ```
      ```
      df.head()
      ```
      
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/be8803ae-b2a5-4fa4-bb4d-e1b176d59d95)
      
      ```
      max_vals =np.max(np.abs(df[['Height','Weight']]))
      max_vals
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/1ac603ce-e8e7-48cb-807e-c75422112f00)
      ```
      from sklearn.preprocessing import StandardScaler
      sc=StandardScaler()
      df[['Height','Weight']]=sc.fit_transform(df[['Height','Weight']])
      df.head(10)
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/b547a110-1a86-45f4-b9aa-635d4d225152)
      ```
      from sklearn.preprocessing import MinMaxScaler
      ```
      ```
      Scaler = MinMaxScaler()
      df[['Height','Weight']]= Scaler.fit_transform(df[['Height','Weight']])
      ```
      ```
      df.head(10)
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/3f5269c5-29e7-48d4-8ac1-e885aceee236)
      ```
      from sklearn.preprocessing import Normalizer
      Scaler = Normalizer()
      df[['Height','Weight']]=Scaler.fit_transform(df[['Height','Weight']])
      df
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/e17107bf-9469-4f02-ac27-2e5ef38a2650)
      ```
      df3=pd.read_csv("/content/bmi.csv")
      ```
      ```
      from sklearn.preprocessing import MaxAbsScaler
      scaler = MaxAbsScaler()
      df3[['Height','Weight']]=scaler.fit_transform(df3[['Height','Weight']])
      df3
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/c31bb172-de4a-437b-9bcb-b0bfa4bd2d8b)
      ```
      df4=pd.read_csv("/content/bmi.csv")
      ```
      ```
      from sklearn.preprocessing import RobustScaler
      scaler = RobustScaler()
      df4[['Height','Weight']]=scaler.fit_transform(df4[['Height','Weight']])
      df.haed(4)
      ```
      ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/ccf7172d-df6b-49d1-9760-2a90ed7dee7c)
      ### KNN CLASSIFION
      ```
      #To work with dataframes

     import pandas as pd

     #To perform numerical operations

     import numpy as np

     #To visualize data

     import seaborn as sns
     ```
     ```
     data = pd.read_csv('/content/income(1) (1).csv' ,na_values=[" ?"])
     data
     ```
     ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/2e5fa3ea-69db-423c-87af-11a200f2c753)
     ```
     data.isnull().sum()
     ```
     ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/c1d4df9d-359c-4789-94a2-d7cecbc38837)
     ```
     data2 = data.dropna(axis=0)
     data2
     ```
     ![image](https://github.com/Krishnakanth23006762/EXNO-4-DS/assets/138849446/4b42882d-cdaa-4096-a765-7781d68598db)


      
# RESULT:
       # INCLUDE YOUR RESULT HERE
