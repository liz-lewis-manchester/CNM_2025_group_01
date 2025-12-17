# importing necessary libraries 
import numpy as np 
import pandas as pd 
import   matplotlib  # as plot #uses as plotting graph  
from scipy. interpolate import interp1d
path= "/content/initial_conditions.csv"   #define the CSV data file path and read CSV file into pandas DataFrame

# reading the data, 'latin1' encoding handles special characters if present in the file
df=pd.read_csv(path, encoding = 'latin1') 
array_data = df.to_numpy()  # converting data to numpy array
x=
y=
f = interp1d(x, y, kind='linear')  

# generate 10 points between each interval
num_between = 5
x_new = np.linspace(x[0], x[-1], (len(x) - 1) * num_between + 1)

# evaluate interpolation
y_new = f(x_new)

print("x_new:", x_new)
print("y_new:", y_new)
