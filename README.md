# CNM_2025_group_01
import numpy as np
import pandas as pd
import matplotlib as plt
url= [initial_conditions.csv](https://github.com/liz-lewis-manchester/CNM_2025_group_01/blob/88c6e83620671f52e62863c5f3f7ef4a028f2a05/initial_conditions.csv)
df=pd.read_csv(url)
array_data = df.to_numpy()
print(array_data)
