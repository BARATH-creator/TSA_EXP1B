# Ex.No: 1B                     CONVERSION OF NON STATIONARY TO STATIONARY DATA
# Date: 11/03/25

### AIM:
To perform regular differncing,seasonal adjustment and log transformatio on international airline passenger data
### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the data preprocessing if needed and apply regular differncing,seasonal adjustment,log transformation.
4. Plot the data according to need, before and after regular differncing,seasonal adjustment,log transformation.
5. Display the overall results.
### PROGRAM:
```
DEVELOPED BY:S.BARATH
REGISTER NUMBER:212224240022
```
```py
from matplotlib import pyplot as plt
import pandas as pd

df=pd.read_csv("/content/test.csv")

df.head()

df['Month']=pd.to_datetime(df['Month'])


df.dtypes

df.set_index('Month',inplace=True)

df_resampled = df['#Passengers'].resample('D').interpolate()
df_resampled.plot(kind='line',label='Total Sales', color='black')
plt.title('Time Series Plot of Number of passengers ecah day')
plt.xlabel('Day')
plt.ylabel('Number of passengers')
plt.legend()
plt.grid(True)
plt.show()
```


### OUTPUT:
![735fa0f2-5e44-40f3-9758-f10d914525e2](https://github.com/user-attachments/assets/81c242ab-6d5d-4549-bfc6-8cf81a683083)



### RESULT:
Thus we have created the python code for the conversion of non stationary to stationary data on international airline passenger
data.
