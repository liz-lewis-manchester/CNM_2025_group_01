# CNM_2025_group_01
import numpy as np
import pandas as pd
import matplotlib as plt
url= [initial_conditions.csv](https://github.com/liz-lewis-manchester/CNM_2025_group_01/blob/88c6e83620671f52e62863c5f3f7ef4a028f2a05/initial_conditions.csv)
df=pd.read_csv(url)
array_data = df.to_numpy()
df.columns = df.columns.str.strip().str.replace('\ufeff', '')
x = df["Distance (m)"].values
y = df["Concentration (µg/m_)"].values 
# Number of new points BETWEEN each original pair
N = 10
new_x = []
new_y = []

for i in range(len(x)-1):
    # Create N+2 points including both ends (e.g., 4 points for N=2)
    xi = np.linspace(x[i], x[i+1], N+2)
    yi = np.linspace(y[i], y[i+1], N+2)
# Add all except last (to avoid repeating next segment's first point)
    new_x.extend(xi[:-1])
    new_y.extend(yi[:-1])
# Add the final data point
new_x.append(x[-1])
new_y.append(y[-1])

