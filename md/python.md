#### help
`pydoc <package-name> | less`
<details>   
    <summary>Install less for windows</summary>
    <b>Winget</b><br>
    winget install jftuga.less<br>
    <b>Chocolatey</b><br>
    choco install less<br>
    <b>Scoop</b><br>
    scoop install less<br>
</details>

#### Numpy 
`pip install numpy`
```py

# Initialization
np_array = np.array(<list>) 

# Element Wise Calculations
np_array_new = np_array (operator) (expression)
bool_array = np_array (comparision_operator) (operand) 

# Subsetting
np_array_new = np_array[np_array (comparision_operator) (operand)]

# Accessing and slicing
np_array_new = np_array[i, x:y]

# Numpy Methods
np_array_new = np.concatenate(np_array_i, np_array_j)
np_array_new = np.stack((np_array_i, np_array_j), axis = 0,1,None) 
np_array_new = np.where(condition, x, y)
np_array_new = np.sort(np_array)

```

#### Pandas
`pip install pandas`

```py

# Pandas Series
pd_Series = pd.Series(array, index_array) 
pd_Series = pd.Series(dict)

# Read CSV Files
df = pd.read_csv("path", index_col="colname") 

# Parse dataframes
df.head(row_count)
df.tail(row_count)
df.info()
df.columns
df.rename(columns={
    'old_colname_1': 'new_colname_1',
    'old_colname_2': 'new_colname_2',
    ...
}, inplace=True)

df.columns = [col.lower() for col in df] # ! for col in df : dataframe iterator is always a column by design

# Describe dataframes
df.describe()
df.shape() 
df['colname'].describe()
df.colname.value_counts()
df['colname'].max()
df['colname'].min()
df['colname'].mean()
df['colname'].median()
df['colname'].std()
df['colname'].count() # ! NON NULL VALUES
df_concat = pd.concat([df_i, df_j])

# Complex dataframe methods
df.groupby('colname_i').colname_j.mean()
pd.pivot_table(df, index=[i,j,..], values=['colname'], aggfunc=[np.methodname()])

# Data Cleaning
df_j = df_i.drop_duplicates()
df.drop_duplicates(inplace=True)
df_concat.drop_duplicates(inplace=True, keep='first','last',False) # ! False means that if a row has a twin, throw both row and its twin

# Null values
df.isnull() # ! RETURNS A BOOLEAN DATAFRAME WHERE THE CELL THAT IS NULL IS TRUE
df.isnull().sum() 
df.isnull().sum().sum()
df.dropna(inplace=True, axis=0,1) 

```

#### Data Visualization
`pip install seaborn`
`pip install matplotlib`

```py
from matplotlib import pyplot as plt
```




