# Data-Analytics
import pandas as pd#importing the pandas lib
import numpy as np#importing nnumpy lib

url1 = "/content/sample_data/california_housing_test.csv"# url for dataset1
data1 = pd.read_csv(url1) #reading the dataset

url2 = "/content/sample_data/california_housing_train.csv"# url for dataset2
data2 = pd.read_csv(url2)#reading dataset 2

cc_data = pd.concat([data1, data2], ignore_index=True)

merge_data = pd.merge(data1, data2, how="outer", on=["longitude", "latitude"])


print("Concatenated Data - First few rows:")
print(cc_data.head())

print("Merged Data - First few rows:")
print(merge_data.head())
