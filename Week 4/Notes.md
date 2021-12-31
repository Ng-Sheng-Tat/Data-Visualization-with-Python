## Week 4
**Dashboard**: a responsive real-time data board can help to answer business question easily
Tools include plotly, voila, panel, streamlit, bokeh, flask, ipywidget, matplotlib, bowtie, etc.

**Plotly** library for interactive charts, that can be publish in web easily

**Plotly Sub-modules**
1. Plotly Graph Objects: Low-level interface to figures, traces and layout
  - ``plotly.graph_objects.Figure``
2. Plotly Express: High-lvel wrapper
```
import plotly.graph_objects as go
import plotly.express as px
import numpy as np

fig = go.Figure(data=go.Scatter(x=xdata, y=ydata))
fig.update_layout(title='title', xaxis_title='xtitle', yaxis_title='ytitle')
fig.show()
```
**Alternatively**
```
fig = px.line(x=xdata, y=ydata, title='title', labels=dict(x='xtitle'm y='ytitle'))
fig.show()
````
---
**Dash** library, an open source UI Python Library from Plotly, support multi platform
1. Layout -> what to plot
2. Components -> Interactivity, comprises of core and html component
---
**Dash - Callbacks**
Callback is a python function that are automatically called by Dash whenever an input component's property changes. Decorator includes **@app.callback**
```
@app.callback(Output, Input)
def callback_function:
  ...
  ...
  return some_result
```
---
**Lesson Summary**

- Best dashboards answer critical business questions. It will help business make informed decisions, thereby improving performance.

- Dashboards can produce real-time visuals.

- Plotly is an interactive, open-source plotting library that supports over 40 chart types.

- The web based visualizations created using Plotly python can be displayed in Jupyter notebook, saved to standalone HTML files, or served as part of pure Python-built web applications using Dash.

- Plotly Graph Objects is the low-level interface to figures, traces, and layout whereas plotly express is a high-level wrapper for Plotly.

- Dash is an Open-Source User Interface Python library for creating reactive, web-based applications. It is both enterprise-ready and a first-class member of Plotly’s open-source tools.

- Core and HTML are the two components of dash.

- The dash_html_components library has a component for every HTML tag.

- The dash_core_components describe higher-level components that are interactive and are generated with JavaScript, HTML, and CSS through the React.js library.

- A callback function is a python function that is automatically called by Dash whenever an input component's property changes. Callback function is decorated with `@app.callback` decorator.

- Callback decorator function takes two parameters: Input and Output. Input and Output to the callback function will have component id and component property. Multiple inputs or outputs should be enclosed inside either a list or tuple.
