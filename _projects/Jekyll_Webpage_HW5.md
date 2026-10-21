---
name: Jekyll Webpage HW5
tools: [Python, HTML, vega-lite,Altair]
image: assets/pngs/cars.png
description: This is a project that uses vega-lite for interactive viz using the bigfoot sighting dataset!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# HW 5 Visuals

## Visual 1
Visual one shows every reported bigfoot sighting in the United States. You can use the slider to change the year and use the dropdown menu to change the class of sighting. The visualizations lets us see where bigfoot appears and when allowing us to possibly deduce a pattern.

We can use a vegachart HTML tag like so:

```
<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_map.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/bigfoot_map.json" style="width: 100%"></vegachart>

## Visual 2

Visual 2 shows a line chart showing the growth and decline of reported bigfoot sightings starting in 1870 - 2018. 
```
<vegachart schema-url="{{ site.baseurl }}/assets/json/year_line.json" style="width: 100%"></vegachart>
```

<vegachart schema-url="{{ site.baseurl }}/assets/json/year_line.json" style="width: 100%"></vegachart>



## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/coltonmurph/coltonmurph.github.io/blob/main/python_notebooks/Jekyll_Webpage_Workbook.ipynb" text="The Analysis" %}
</div>

