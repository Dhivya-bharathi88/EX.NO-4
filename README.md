
# Ex-no.4 Bivariate and Multivariate Analysis

# AIM:

To perform Bivariate and Multivariate Analysis for the given data set.

# EXPLANATION:

Bivariate analysis is the simultaneous analysis of two variables. It explores the concept of the relationship between two variable whether there exists an association and the strength of this association or whether there are differences between two variables and the significance of these differences. Multivariate is an extension of bivariate analysis which means it involves multiple variables at the same time to find correlation between them. Multivariate Analysis is a set of statistical model that examine patterns in multidimensional data by considering at once, several data variable.

# ALGORITHM:

#STEP-1:

Read the given data.

# STEP-2:

Get the information about the data.

# STEP-3:

Perform Bivariate Analysis Techniques for the given dataset.

# STEP-4:

Perform Multivariate Analysis Techniques for the given dataset.

# STEP-5:

Save the cleaned data to the file.

# CODE:

# BIVARIATE ANALYSIS:

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

# MULTIVARIATE ANALYSIS:

import pandas as pd

import numpy as np

import seaborn as sns

from google.colab import files

uploaded = files.upload()

df = pd.read_csv("SuperStore.csv")

df.corr()

sns.heatmap(df.corr(),annot=True)

# OUTPUT:
![Screenshot (101)](https://user-images.githubusercontent.com/128019999/232210473-8185c5f9-6a5a-49b2-877e-6b4c9774d5d9.png)
![Screenshot (102)](https://user-images.githubusercontent.com/128019999/232210527-dd5d1cc8-ddd9-4c02-b632-e2267f8e1e39.png)
![Screenshot (103)](https://user-images.githubusercontent.com/128019999/232210538-43b820d7-bf6d-4e89-85e9-0646a7deda83.png)
![Screenshot (104)](https://user-images.githubusercontent.com/128019999/232210552-a5d7dcd8-d527-4f4d-9984-e03ea1da87c6.png)
![Screenshot (105)](https://user-images.githubusercontent.com/128019999/232210558-d9885f4e-afdd-47b7-9c68-69acdaf060d5.png)
![Screenshot (106)](https://user-images.githubusercontent.com/128019999/232210568-65153e64-013a-4543-b8fc-a030d4991eaa.png)
![Screenshot (107)](https://user-images.githubusercontent.com/128019999/232210580-e9531db2-841a-493a-9908-671a7e5daa4f.png)
![Screenshot (108)](https://user-images.githubusercontent.com/128019999/232210585-c619a29e-05c7-4fe3-b856-2ebdf0ea4be1.png)
![Screenshot (109)](https://user-images.githubusercontent.com/128019999/232210592-658a5fac-9e79-4799-9c3c-af4a07974ba5.png)
![Screenshot (110)](https://user-images.githubusercontent.com/128019999/232210603-37d4c09e-940e-43ee-afdc-365148290749.png)
![Screenshot (111)](https://user-images.githubusercontent.com/128019999/232210616-2de508a1-8e54-4872-9245-c693b4753620.png)
![Screenshot (112)](https://user-images.githubusercontent.com/128019999/232210630-0bf09d50-c234-4eae-bdba-b5b9780416b9.png)
![Screenshot (113)](https://user-images.githubusercontent.com/128019999/232210644-01a88b55-53e6-4ddc-9b85-5ce1f71cc177.png)

# RESULT:

Thus the Bivariate and Multivariate Analysis for the given data set is executed and output was verified successfully.
