## Week 1
**Visual Representations** is for:
1. Exploratory Data Analysis
2. Communicate clearly the data
3. Shared unbiased representation of data
4. Use them to support recommendations to different stakeholders
**Simple Concept**
1. Less is more effective
2. Less is more attractive
3. Less is more imperative
---
**Matplotlib Architecture**
- sync with MATLAB, has interface to operate it as well
1. Backend Layer (FigureCanvas, Renderer, Event)
  - for professionals
2. Artist Layer (Artist)
3. Scripting Layer (pyplot)
  - for beginner
---
**Learning Matplolib in scripting interface**
```
%matplotlib inline

%matplotlib notebook - UI control

import matplotlib.pyplot as plt

plt.plot(n,m,'o')

plt.xlabel("X")
plt.ylabel("Y")
plt.title("Plotting Title")
plt.show()
```
**Well support for Pandas**
``df.plot(kind='line')``
``df.plot(kind='hist')``
---
**Importing Data for plotting and analysis**
```
import numpy as np
import pandas as pd
from __future__ import print_function

!pip install xlrd

df = pd.read_excel('url', sheetname='', skiprows=range(n), skip_footer=n)

df.head()
```
---
**Line Plot** for continuous data
```
import matplotlib.pyplot as plt
import matplotlib as mpl

years = list(map(str, range(year1, year2)))

df.loc['column', years].plot(kind='line')
plt.title('')
plt.xlabel('')
plt.ylabel('')

plt.show()
```
