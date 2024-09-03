# Ex.No: 01A PLOT A TIME SERIES DATA
### DEVELOPED BY:RAGUNATH R
### REGISTER NO:21222224081
###  Date: 

# AIM:
To Develop a python program to Plot a time series data, electric production (date/daily minimum temperature).

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Plot the data according to need and can be altered monthly, or yearly.
4. Display the graph.
# PROGRAM:

```
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
file_path ='/content/daily-minimum-temperatures-in-me.csv'# Replace with your file path
data = pd.read_csv(file_path)

# Convert the 'Date' column to datetime format
data['Date'] = pd.to_datetime(data['Date'], format='%m/%d/%Y')

# Set the 'Date' column as the index
data.set_index('Date', inplace=True)

# Plot the time series data
plt.figure(figsize=(10, 6))
plt.plot(data.index, data['Daily minimum temperatures'], color='blue', label='Daily Minimum Temperatures')
plt.title('Daily Minimum Temperatures Over Time')
plt.xlabel('Date')
plt.ylabel('Temperature (°C)')
plt.legend()
plt.grid(True)
plt.show()

```



# OUTPUT:
![image](https://github.com/user-attachments/assets/a1309e86-a3bb-4f18-aaff-e76b243830fd)





# RESULT:
Thus,the Python code has been created to visualize the time series of the given data.
