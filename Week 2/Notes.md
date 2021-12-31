## Week 2
**Area Plot**
- also known as area chart or area graph
- use to demonstrate cumulative parameter of interest
```
years = list(map(str, range(year1, year2)))

df.sort_values(['column1'], ascending=False, axis=0, inplace=True)

dftop5 = df.head()
dftop5 = dftop5['column'].transpose()

import matplotlib.pyplot as plt
import matplotlib as mpl

dftop5.plot(kind='area')
dftop5.title('')
plt.show()
```

**Histogram** : data is cast into number of bins first
```
import numpy as np

count, bin_edges = np.histogram(df)

df.plot(kind='hist', xticks=bin_edges)
```

**Bar Chart**: shows the frequency
``kind='bar'``

**Pie Chart**: shows the frequency (less preferred chart)
``df.groupby('columnname', axis=0).sum()``
``kind='pie'``

**Box Plot**: shows various statistical inferences and parameters' locations
``df.loc[['column'], years].transpose()``
``kind='box'``

**Scatter Plot** to show relationship between dependent and independent variables (two-dimensional only)
``df.plot(kind='scatter', x='xcolumn', y='ycolumn')``
