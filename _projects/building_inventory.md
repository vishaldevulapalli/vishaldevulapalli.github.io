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
### Write-Up
#### Description
The bar chart represents the top 10 cities with the highest total building square footage. This visualization highlights which cities have the most significant infrastructure in terms of area, providing insights into the spatial distribution of large buildings.

#### Design Choices
The chart uses a descending order bar layout, ensuring the most impactful cities are displayed prominently at the top. A gradient color scheme emphasizes the differences in square footage, making it easy to compare across cities. Tooltips were added to allow users to hover over each bar for precise details about square footage and city name.

#### Data Transformations
The dataset was grouped by city, and the total square footage for each city was calculated. The data was then sorted in descending order, and only the top 10 entries were selected for the visualization. This aggregation ensures the chart remains focused and free from noise.

#### Changes from Homework 7
This chart extends the previous homework by incorporating interactive tooltips and a more refined sorting mechanism. Additionally, the presentation was enhanced with a visually appealing gradient color palette, making the data differences more pronounced.

#### Interactivity
Interactivity in this chart comes through hover-enabled tooltips, which display detailed information for each city. This feature helps users quickly access additional context without cluttering the visualization.

---

### **2. Square Footage by Year Acquired**
This scatter plot, combined with a dynamic trend line, visualizes square footage trends over time. A dropdown filter allows users to select specific cities.

<vegachart schema-url="{{ site.baseurl }}/assets/json/scatter_plot.json" style="width: 100%"></vegachart>
### Write-Up
#### Description
The scatter plot explores the relationship between square footage and the year of acquisition, offering a temporal perspective on building infrastructure trends. A dynamic trend line overlays the scatter points to illustrate the overall trend.

#### Design Choices
The visualization employs a color-coded scheme based on city names, allowing viewers to identify patterns by location. The scatter points are semi-transparent to prevent overlap from obscuring details, while the trend line is highlighted in red to stand out clearly.

#### Data Transformations
The data was filtered to exclude records with missing or incomplete information for square footage or acquisition year. It was further cleaned to ensure accurate regression modeling for the trend line, and categorical city names were retained for color-coding.

#### Changes from Homework 7
Compared to Homework 7, this scatter plot integrates an interactive dropdown filter for city selection and a regression-based trend line. These enhancements make the visualization more user-focused and insightful.

#### Interactivity
The dropdown filter allows users to focus on specific cities, while hover-enabled tooltips provide precise details for each data point, including city name, square footage, and acquisition year. This interactivity improves user engagement and enhances the clarity of the trends displayed.

---

## Data and Analysis

Below are links to the dataset and Python notebook used for the analysis:

<div class="left">
{% include elements/button.html link= "https://github.com/vishaldevulapalli/vishaldevulapalli.github.io/blob/main/assets/building_inventory.csv" text="The Dataset" %}
</div>

<div class="right">
{% include elements/button.html link= "https://github.com/vishaldevulapalli/vishaldevulapalli.github.io/blob/main/python_notebooks/Visualizations.ipynb" text="The Analysis Notebook" %}
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
