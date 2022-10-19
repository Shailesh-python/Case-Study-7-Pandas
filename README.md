# Case Study #7 Balanced Tree

<img src='https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)'/>
<img src='https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)'/>

The following are my solutions to the Case Study 7 Balanced Tree questions in 
[Danny Ma's Serious SQL course](https://www.datawithdanny.com/ "Data With Danny")
<br/>
<br/>
There are 4 [data tables](https://github.com/Shailesh-python/Case-Study-7-Balanced-Tree/blob/main/Data%20Sets) available to us in `balanced_tree` schema which we can use to run our SQL queries with:

1. `Product Details`

2. `Product Sales`

3. `Product Hierarcy`

4. `Product Price`

```python
import pandas as pd
import numpy as np
import pyodbc as py
import numpy as np

import warnings
warnings.filterwarnings('ignore')
```

```python
conn = py.connect(
    "DRIVER={SQL Server};SERVER=SHAILESH-PC\SQLEXPRESS;DATABASE=DannyMa;"
)

df_sales = pd.read_sql_query('select * from balanced_tree.sales',conn)
df_pp = pd.read_sql_query('select * from balanced_tree.product_prices',conn)
df_ph = pd.read_sql_query('select * from balanced_tree.product_hierarchy',conn)
df_pd = pd.read_sql_query('select * from balanced_tree.product_details',conn)

conn.close()
```
[Check my solution](https://github.com/Shailesh-python/Case-Study-7-Pandas/blob/main/Case%20Study%207%20Solutions.ipynb)
