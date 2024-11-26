---
name: Building Inventory Analysis
tools: [Python, HTML, Altair, JSON]
image: assets/json/building_inventory.png
description: This project uses Altair to create interactive visualizations based on the Building Inventory dataset.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Building Inventory Analysis

This project showcases interactive data visualizations generated with Altair and Python using the Building Inventory dataset. The dataset contains information about square footage, building acquisition years, and more.

## Visualization Highlights

### **1. Top 10 Cities by Total Square Footage**
This bar chart highlights the top 10 cities with the highest total building square footage.

<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>

---

### **2. Square Footage by Year Acquired**
This scatter plot, combined with a dynamic trend line, visualizes square footage trends over time. A dropdown filter allows users to select specific cities.

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot.json" style="width: 100%"></vegachart>

---

## Data and Analysis

Below are links to the dataset and Python notebook used for the analysis:

<div class="left">
{% include elements/button.html link= "https://github.com/vishaldevulapalli/vishaldevulapalli.github.io/blob/main/assets/building_inventory.csv" text="The Dataset" %}
</div>

<div class="right">
{% include elements/button.html link="/python_notebooks/Visualizations.ipynb" text="The Analysis Notebook" %}
</div>

## Methods and Tools

This project uses:
- **Python & Altair**: To create the visualizations and export them to JSON.
- **Jekyll**: To integrate the visualizations into this static webpage.
- **Building Inventory Dataset**: A dataset showcasing building details, acquisition years, and square footage.

## About the Visualizations

1. **Bar Chart**: Displays the top 10 cities by total building square footage.  
   - **Interactive Features**: Tooltip for city name and square footage details.

2. **Scatter Plot with Trend Line**: Visualizes square footage trends over years with interactive filters.
   - **Interactive Features**: Dropdown filter by city, trend line, and hover details.

---

## Embed Code Snippets

### **Bar Chart**
```html
<vegachart schema-url="{{ site.baseurl }}/assets/json/bar_chart.json" style="width: 100%"></vegachart>
```
### **Scatter Plot with Trend Line**
```html
<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot.json" style="width: 100%"></vegachart>
```
