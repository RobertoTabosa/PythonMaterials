```python
# Loading data into Pandas
```


```python
import pandas as pd
df = pd. read_csv("pokemon_data.csv")
print (df.head(2))
print (df.tail(2))
```


## EDA(Exploratory Data Analysis)


```python
## EDA(Exploratory Data Analysis)

https://www.youtube.com/watch?v=4sxhE3wP3Ug
Possible steps:
#1. import libraries
      import pandas as pd
      import datetime as dt  
#2. Readinf file
      v_name_base = pd.read_csv ("path/filename") 
#3. Visualize the base
      v_name_base.head()
      v_name_base.tail()
#4. Knowing size's base
      v_name_base.shape      # will return amount of rows and columns
      display (v_name_base)  # will return 5 first and last records and the amount of rows and columns
#5. Discovering the analysis period
      start = pd.datetime(v_name_base["name_field"]).dt.date.min()
      end = pd.datetime(v_name_base["name_field"]).dt.date.max()
#6. Check null values and data type
      v_name_base.info ()
#7. Another way to verify type of data
      v_name_base.dtypes ()
#8. Another way to verify null fields
      v_name_base.isnull().sum()
#9. Understanding better null values
      v_name_base["name_file"].value_counts()
      # If a column has just "F" or "T" as possible result, "1" or "0"or whatever binary possibility, AND JUST appear one of then and others Null, we can think on possibility to fill up the null fields with the another value.
#10. Analizing statistics information
      v_name_base.describe() # will return the quarters, mean, std etc
# 11. Understanding a little more this informataion
      v_name_base.plot (kind = "box", figsize=(10,6), subplots=True);
# 12. Now that we understood a little more our base, we can undertand what are the outliers
      v_name_base[v_name_base["column_name"] >= number_whe_want_understand]
      v_name_base.column_name.value_counts()    
      v_name_base.column_name.value_counts().plot(kind="bar");
      v_name_base["Viewership Score"].hist();
      v_name_base[v_name_base["column_name"] == v_name_base["column_name"].max()]
    
    
```


```python
#df.plot (kind = "box", figsize=(10,6), subplots=True);
df.Attack.value_counts().plot(kind="bar");
```


    
![png](output_20_0.png)
    



```python

```
https://www.youtube.com/watch?v=Ewgy-G9cmbg
