import numpy as np
import pandas as pd
import matplotlib as plt
from scipy.interpolate import interp1d
path= "/content/initial_conditions.csv"
df=pd.read_csv(path, encoding = 'latin1')

array_data = df.to_numpy()
f = interp1d(x, y, kind='linear')

# generate 10 points between each interval
num_between = 5
x_new = np.linspace(x[0], x[-1], (len(x) - 1) * num_between + 1)

# evaluate interpolation
y_new = f(x_new)

print("x_new:", x_new)
print("y_new:", y_new)
