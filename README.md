# Ex-no.4 Bivariate and Multivariate Analysis

# AIM:
  To perform Bivariate and Multivariate Analysis for the given data set.

# EXPLANATION:
  Bivariate analysis is the simultaneous analysis of two variables. It explores the concept of the relationship between two variable whether there exists an association and the strength of this association or whether there are differences between two variables and the significance of these differences. Multivariate is an extension of bivariate analysis which means it involves multiple variables at the same time to find correlation between them. Multivariate Analysis is a set of statistical model that examine patterns in multidimensional data by considering at once, several data variable.

# ALGORITHM:

## STEP-1:
  Read the given data.
## STEP-2: 
  Get the information about the data.
## STEP-3: 
  Perform Bivariate Analysis Techniques for the given dataset.
## STEP-4:
  Perform Multivariate Analysis Techniques for the given dataset.
## STEP-5: 
  Save the cleaned data to the file.
  
# CODE:

## BIVARIATE ANALYSIS:

import pandas as pd

import numpy as np

import seaborn as sns

from google.colab import files

uploaded = files.upload()

df = pd.read_csv("SuperStore.csv")

print(df)

df.describe()

df.info()

sns.scatterplot(x=df['Row ID'],y=df['Order ID'])

sns.scatterplot(x=df['Row ID'],y=df['Ship Date'])

import pandas as pd

import numpy as np

import seaborn as sns

from google.colab import files

uploaded = files.upload()

df = pd.read_csv("SuperStore.csv")

states=df.loc[:,["Ship Mode","Postal Code"]]

states=df.loc[:,["Ship Mode","Postal Code"]]

states=states.groupby(by=["Ship Mode"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Ship Mode")

plt.ylabel=("Postal Code")

plt.show()

states=df.loc[:,["Customer Name","Postal Code"]]

states=states.groupby(by=["Customer Name"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Customer Name")

plt.ylabel=("Postal Code")

plt.show()

states=df.loc[:,["Customer ID","Postal Code"]]

states=states.groupby(by=["Customer ID"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Customer ID")

plt.ylabel=("Postal Code")

plt.show()

states=df.loc[:,["Segment","Postal Code"]]

states=states.groupby(by=["Segment"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Segment")

plt.ylabel=("Postal Code")

plt.show()

states=df.loc[:,["Country","Postal Code"]]

states=states.groupby(by=["Country"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Country")

plt.ylabel=("Postal Code")

plt.show()

states=df.loc[:,["City","Postal Code"]]

states=states.groupby(by=["City"]).sum().sort_values(by="Postal Code")

plt.figure(figsize=(17,7))

sns.barplot(x=states.index,y="Postal Code",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("City")

plt.ylabel=("Postal Code")

plt.show()

## MULTIVARIATE ANALYSIS:

import pandas as pd

import numpy as np

import seaborn as sns

from google.colab import files

uploaded = files.upload()

df = pd.read_csv("SuperStore.csv")

df.corr()

sns.heatmap(df.corr(),annot=True)

# OUTPUT:

![WhatsApp Image 2023-04-14 at 10 03 38 PM (1)](https://user-images.githubusercontent.com/128498431/232178443-0014e77b-9716-45ff-ae5e-048f8f220b41.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 36 PM](https://user-images.githubusercontent.com/128498431/232178393-0d179ed4-48ff-4bf4-a726-a32751074201.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 36 PM (1)](https://user-images.githubusercontent.com/128498431/232178413-1cb38f46-8222-4f1f-8238-5d56dd8aa072.jpeg)

![Screenshot (32)](https://user-images.githubusercontent.com/128498431/232178331-62ab89c3-e01a-42e7-b723-c4890ecf3e7c.png)

![Screenshot (31)](https://user-images.githubusercontent.com/128498431/232178366-4ed82f30-286b-494f-96a4-3478f8f26dd0.png)

![WhatsApp Image 2023-04-14 at 10 03 38 PM](https://user-images.githubusercontent.com/128498431/232178521-a1ee48e0-70eb-4e0b-a6b8-4f39abfa6613.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 39 PM (1)](https://user-images.githubusercontent.com/128498431/232178531-3adfac78-11ed-457f-8142-bbaf68ef7ac0.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 40 PM (2)](https://user-images.githubusercontent.com/128498431/232178570-0e2ead94-faa2-4caa-ac01-d0525c31a5a9.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 39 PM (2)](https://user-images.githubusercontent.com/128498431/232178579-c7fd7a19-3a3c-467b-8e0f-08e7372f41e7.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 40 PM](https://user-images.githubusercontent.com/128498431/232178607-e3236656-32de-402a-80cb-c04e45237587.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 40 PM (1)](https://user-images.githubusercontent.com/128498431/232178621-b4cbc458-978d-4382-a491-2d9a5b63a627.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 39 PM](https://user-images.githubusercontent.com/128498431/232178648-4ea8bae6-a7dc-435b-9e35-85e7fb53ad8e.jpeg)

![WhatsApp Image 2023-04-14 at 10 03 41 PM](https://user-images.githubusercontent.com/128498431/232178665-64bf12ac-7bf0-42ac-adbd-17b90d7e9715.jpeg)

# RESULT:
  Thus the Bivariate and Multivariate Analysis for the given data set is executed and output was verified successfully.









