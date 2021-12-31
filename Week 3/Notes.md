## Week 3
**Waffle Charts** to display progress towards goal
- there is no default kind in matplotlib, need to create by your own

**Word Clouds** shows the frequency of the word appearing in an essay
- matplotlib does not support this kind of plot

**Regression Plots** is plot using **seaborn library** which is based on matplotlib and usually for interaction use case and quite powerful.
```
import seaborn as sns
ax = sns.regplot(x='year', y='total', data=df, color='green', marker='+')
```

**Folium** is a powerful Python Library that helps to create several types of Leaflet maps. It enables both the binding of data to a map for choropleth visualizations as well as passing visualizations as markers on the map. The library has a number of built-in tilesets from OpenStreetMap, Mapbox, and Stamen, and supports custom tilesets with Mapbox API keys.

**Create a world map**
```
worldmap = folium.Map(location=[val1, val2], zoom_start=4, tiles='Stamen Toner or Stamen Terrain')
worldmap

# create a feature group
ontario = folium.map.FeatureGroup()

ontario.add_child(
  folium.features.CircleMarker(
    [val1, val2], radius=n,
    color='red', fill_color='red'
    )
  )

worldmap.add_child(ontario)

# label the marker
folium.Marker([val1, val2], popup='Ontario').add_to(worldmap)
```

**Choropleth Maps**: heat maps to show density parameters in applying to a world maps, it is needing a geojson files.
- refers to images
