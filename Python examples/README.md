# Python Examples

* Examples using the in-class dataset (sales data)

## Basic Pandas plotting

![image-20240607154023117](images/image-20240607154023117.png)

![image-20240606142716821](images/image-20240606142716821.png)

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import pandas as pd
import matplotlib.pyplot as plt

df = dataset

df['order_date'] = pd.to_datetime(df['order_date'])
df = df.set_index('order_date')

df.plot(subplots=True)
plt.show()
```

## Seaborn Boxplot with Slicers

![image-20240607154042718](images/image-20240607154042718.png)

![image-20240606142754444](images/image-20240606142754444.png)

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue, stock, price, category)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import seaborn as sns
import matplotlib.pyplot as plt

sns.boxplot(data=dataset, x='sales', y='category')


plt.show()
```

## Seaborn Violinplot with Slicers

![image-20240607154054417](images/image-20240607154054417.png)

![image-20240606142830879](images/image-20240606142830879.png)

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue, stock, price, category)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import seaborn as sns
import matplotlib.pyplot as plt

sns.violinplot(data=dataset, x='sales', y='category', hue='storetype_id')


plt.show()

```

### Seaborn Jointplot with Slicers

![image-20240607154113920](images/image-20240607154113920.png)

![image-20240606142906764](images/image-20240606142906764.png)

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue, stock, price, category)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import seaborn as sns
import matplotlib.pyplot as plt

sns.jointplot(data=dataset, x='revenue', y='sales', hue='category')

plt.show()
```



## Statsmodels with other native charts

![image-20240607154132412](images/image-20240607154132412.png)

![image-20240606143930694](images/image-20240606143930694.png)

**Autocorrelation ACF Plot**

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue, stock, price, category)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import pandas as pd
import matplotlib.pyplot as plt
import statsmodels.api as sm

df = dataset[['order_date', 'sales']]
df = df.set_index('order_date')

sm.graphics.tsa.plot_acf(df, lags=40)

plt.show()
```

**Partial Autocorrelation PACF Plot**

```python
# The following code to create a dataframe and remove duplicated rows is always executed and acts as a preamble for your script: 

# dataset = pandas.DataFrame(order_date, sales, revenue, stock, price, category)
# dataset = dataset.drop_duplicates()

# Paste or type your script code here:

import pandas as pd
import matplotlib.pyplot as plt
import statsmodels.api as sm

df = dataset[['order_date', 'sales']]
df = df.set_index('order_date')

sm.graphics.tsa.plot_pacf(df, lags=40)

plt.show()
```

