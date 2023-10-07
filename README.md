# ODD2023-DataScience-Ex-03
### AIM

To read the given data and perform the univariate analysis with different types of plots.

### ALGORITHM

1. Read the given data.
2. Perform data cleaning process.
3. Visulaize and analyse the data using various plots.

### CODE AND OUTPUT
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
```
df=pd.read_csv("/iris.csv")
df
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/0fe65207-2db4-400c-9fdc-4b3556aa8181)

```
df.nunique()#returns the number of unique values
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/c45ae394-135a-4f07-be51-da2c8ea52300)

```
df.iloc[:,4].value_counts()
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/d658eef2-404f-4d84-939e-a5d5e5eb7f66)

```
for i in range(0,df.shape[1]):
  print("-----------",df.columns[i],"------------")
  print(df.iloc[:,i].value_counts())
  print("---------------------------------------")
```

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/04dc02fe-44fd-468b-a3b9-af9c25aa0988)

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/37d2358d-fa77-4212-8e51-ba4aa4b5e8bd)

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/205f0ac7-faa2-48f4-9a44-bedd79085339)

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/481a483b-4aba-4dd8-9d16-d3df865dbc69)

```
sns.countplot(x='species',data=df)
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/52ee5e48-9acf-4a40-955d-12819d0d0071)

```
dfv=df.loc[df['species']=='virginica']
dfv
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/89f5ae9e-5403-4184-bffe-23f3316a8e0c)

```
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.show()
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/79b63223-dd97-4b5e-8ce0-2128a0b7792b)

```
dfs=df[df['species']=='setosa']
dfs
```
![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/2d3c3ddd-3228-4267-bd1e-790e07516e25)

```
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.xlabel('sepal length')
plt.show()
```

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/dfc91d7a-90ee-4e21-a8ed-67349dd03a28)

```
dfc=df.loc[df['species']=='versicolor']
dfc
```

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/7d85424d-19cc-4759-80d3-fbed617983d4)

```
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'x')
plt.show()
```

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/dc2255f6-9344-4344-9783-5f8722baadfa)

```
plt.plot(dfv['sepal_length'],np.zeros_like(dfv['sepal_length']),'*')
plt.plot(dfs['sepal_length'],np.zeros_like(dfs['sepal_length']),'+')
plt.plot(dfc['sepal_length'],np.zeros_like(dfc['sepal_length']),'x')
plt.xlabel('sepal length')
plt.show()
```

![image](https://github.com/Pranav-AJ/ODD2023-DataScience-Ex-03/assets/118904526/3fcdd602-5283-45d3-a9f8-1600757c2186)
