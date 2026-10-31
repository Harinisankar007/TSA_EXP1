# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# DATASET
DailyDelhiClimateTrain

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
6. 
# PROGRAM:
```python
import pandas as pd
import matplotlib.pyplot as plt
train = pd.read_csv("DailyDelhiClimateTrain.csv")
test = pd.read_csv("DailyDelhiClimateTest.csv")

print("Training Dataset:")
print(train.head())

print("\nTesting Dataset:")
print(test.head())

train['date'] = pd.to_datetime(train['date'])
test['date'] = pd.to_datetime(test['date'])

train.set_index('date', inplace=True)
test.set_index('date', inplace=True)

train['meantemp'].plot(
    kind='line',
    color='black',
    label='Training Mean Temperature'
)

plt.title('Daily Delhi Climate - Time Series Plot')
plt.xlabel('Date')
plt.ylabel('Mean Temperature')
plt.legend()
plt.grid(True)
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

# OUTPUT:
<img width="507" height="257" alt="image" src="https://github.com/user-attachments/assets/1043644f-f6e8-443f-af99-f5af9a009898" />

<img width="619" height="469" alt="image" src="https://github.com/user-attachments/assets/c4abfb5d-8c79-4129-9133-1a4c625f1368" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
