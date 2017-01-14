# Report

## Dataset

The dataset consists of weather data provided by the Central Institution for Meteorology and Geodynamics ([ZAMG](http://www.zamg.ac.at/)) for the weather station *Linz/Hörsching* in Austria for the year 2016.

Since ZAMG does not provide the data directly, the website <http://at-wetter.tk> was used to get the values. This website stores the ZAMG values for all weather stations since 2014 and provides them via a public REST API.

We have *hourly* values for the whole year 2016, which sums up to 8784 total entries. We also have a few missing values for 52 hours out of 8784. These missing values were removed. The following attributes are provided:

  1. Temperature \[°C\]
  1. Dew Point \[°C\]
  1. Relative Humidity \[%\] (range: 0-100)
  1. Wind Direction \[°\] (range: [0-360))
  1. Wind Speed \[km/h\]
  1. Peak Wind Speed \[km/h\]
  1. Precipitation \[l/m²\]
  1. Atmospheric Pressure (sea level) \[hPa\]
  1. Atmospheric Pressure (station level) \[hPa\]
  1. Sunshine \[%\] (range: 0-100)

## Tasks

This visualization project focuses on 3 tasks:

  1. Trend of various attributes
  1. Average wind speed compared to its direction
  1. Relationship between two attributes

The trend describes the value of the attributes (e.g. temperature, rain, ...) over time using a line chart.

Since the wind direction is a cyclic value, the average wind speed can be displayed in an circle area chart. For each direction, the average amount of all the selected wind speed attributes will be calculated and displayed according to its angle. 0° denotes the wind direction "North".

The last diagram shows the relationship between two chosen attributes in a scatter chart.

## Visual Design

The GitHub page is split up into those three sections. The first one is the line chart where a date range can be selected. This selection also affects the other two charts. The circle area chart showing the average wind speed is located in the bottom left section. Next to it, the scatter plot shows the relationship between two selected attributes.

![Visual Design](https://meinsiedler.github.io/zamg-weather-data/assets/img/layout.png)

## Prototype Interaction

In the line chart, the current trend can be chosen at the top. A selection can either be done by drawing a box using the left mouse button, or selecting a month from the dropdown list. This will limit the data, used by all the shown diagrams. Using the "Reset Zoom" button, the current selection can be undone.
The right mouse button can be used to translate the diagram and browse around the trend line. Since this will change the selection, it has an effect on the other diagrams too.

The data used by the scatter plot can be chosen using the two dropdown lists at the top of the diagram.

![Interaction](http://i.imgur.com/noNEjJ6.gif)

## Insight / Conclusion

## How to Start

The project is hosted under <https://meinsiedler.github.io/zamg-weather-data/>.
You can see a running live demo there.

The GitHub repository can be found under <https://github.com/meinsiedler/zamg-weather-data>.
You can check out the source there.

