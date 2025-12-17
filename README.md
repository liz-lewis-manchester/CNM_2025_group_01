import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from scipy.interpolate import interp1d
path = "/content/initial_conditions (5).csv"
df = pd.read_csv(path, encoding='latin1')
array_data = df.to_numpy()  # converting data to numpy array
df.columns = df.columns.str.strip().str.replace('\ufeff', '')
df = df.rename(columns={
    df.columns[0]: 'concentration',
    df.columns[1]: 'distance'})
df['concentration'] = pd.to_numeric(df['concentration'], errors='coerce')
df['distance'] = pd.to_numeric(df['distance'], errors='coerce')
df = df.dropna()
df = df.sort_values(by='concentration')
df = df.drop_duplicates(subset='concentration')
x = df['concentration'].to_numpy()
y = df['distance'].to_numpy()
f = interp1d(x, y, kind='linear', bounds_error=False)
num_between = 5
x_new = np.linspace(x.min(), x.max(), (len(x) - 1) * num_between + 1)
y_new = f(x_new)

extended_df = pd.DataFrame({
    'concentration': x_new,
    'distance': y_new})
extended_df.to_csv("extended_data.csv", index=False)
print(x_new,y_new)
