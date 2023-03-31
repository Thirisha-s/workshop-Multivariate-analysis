# workshop-Multivariate-analysis
# AIM:
To Perform Multivariate Analysis

# ALGORITHM:
# step1:
1.Read the given data

# step2:
2.Get information from the data

# step3
3.Perform the Multivariate Analysis

# step4
4.Save the clean data to file

# PROGRAM:
Name:sthirisha
Register number:212222230160
# Bivariate Analysis
# scatter plot
```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib as plt
df = pd.read_csv("/content/FlightInformation.csv")
sns.scatterplot (df['Price']
```


#  Numerical & Categorical:
# bar plot
```
import pandas as pd
import seaborn as sns
sns.barplot (x=df['Duration'],y=df['Price'])
```
![Screenshot 2023-03-31 113458](https://user-images.githubusercontent.com/120380280/229036703-ec0f4175-f96a-45ec-a4ae-dbe9de7fc7de.png)

sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df)

![Screenshot 2023-03-31 113637](https://user-images.githubusercontent.com/120380280/229036971-fb8c309e-3cc4-4704-9da9-7e83ddf63bdc.png)
```
states=df.loc[:,["Duration","Price"]]
states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")
import matplotlib.pyplot as plt
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("Duration")
plt.ylabel=("Price")
plt.show()
```
![Screenshot 2023-03-31 113810](https://user-images.githubusercontent.com/120380280/229037297-4cd57ab2-46cf-4587-82cb-a7bf5445ee36.png)

# MULTIVARIATE ANALYSIS:
# Categorical & Categorical Heatmap
```
import numpy as np
import seaborn as sn
import matplotlib.pyplot as plt
data=pd.read_csv("/content/FlightInformation.csv")
data = np.random.randint(low = 1, high = 100, size = (10, 10))
print("The data to be plotted:\n")
print(data)
hm = sn.heatmap(data = data)
plt.show()
```
![Screenshot 2023-03-31 114059](https://user-images.githubusercontent.com/120380280/229037766-a67a280d-cedc-4981-a6a0-7471f9f34daa.png)
![Screenshot 2023-03-31 114128](https://user-images.githubusercontent.com/120380280/229037857-327959d6-09af-40fc-be24-8a677da97cd9.png)

# RESULT:
Thus, Bivariate/Multivariate Analysis is performed successfully.


