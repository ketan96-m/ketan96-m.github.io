---
name: Homework10
tools: [Python, HTML, vega-lite, ALTAIR]
# image: assets/pngs/cars.png
description: This is a Assignment 10 by Shruti, Nidhi, Ketan
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---
## Homework10

Assignment 10 by Shruti, Nidhi and Ketan

### Plot 1
<!-- these are written in a combo of html and liquid --> 
***Note: To access interactivity, drag and select a part on the graph and scroll all the way to the right***

<p>The provided visualizations are created using Altair. The first chart is interactive and displays the total square footage of agencies in different cities across the United States. The user has the option to select a particular group of cities from the first chart, which generates charts 2 and 3 based on the selection.It can also be seen that Chicago has the maximum area used by different agencies followed by Springfield and Urbana.</p>
<p>Chart 2 displays the square footage for all agencies in the chosen cities, while Chart 3 is a time-series chart which displays the total square footage of an individual agency against the year it was constructed.</p>
<p>No transformation is done on the data as for the fields we are utilizing there are no null entries.</p>
<p><b>The encoding types used are as below:</b></p>
<ul>
    <li><b>Plot 1:</b> Nominal as the data (City) being plotted is discrete and unordered</li>
    <li><b>Plot 2:</b> Ordinal as the data (Agency) being plotted is discrete and ordered</li>
    <li><b>Plot 3:</b> Nominal as the data (Year Constructed) being plotted is discrete and unordered</li>
</ul>
<p><b>Interactivity used:</b> Interval selection using <i>add_selection</i> method.</p>


<vegachart schema-url="{{ site.baseurl }}/assets/json/SquareFootage.json" style="width: 100%"></vegachart>
<br />
<br />

### Plot 2

<p>The provided visualizations are created using ipywidgets and maplotlib. The first chart is a scatter plot and displays the correlation between the Year Contsructed and the Year Acquired for the selected Agency from the dropdown.</p>
<p>Chart 2 is a bar plot which displays the square footage for all the cities the selected Agency is in. The data has been tarnsformed to add a new column <i>City_zip</i> which contains the City and the different Zip Codes in order to show the square footage separately for each area. Chart 3 is a bar plot chart which displays the total square footage of the selected  agency against the year it was constructed.</p>

<p><b>Interactivity used:</b> Dropdown selection using <i>ipywidegts.interact</i> method.</p>


![]({{site.baseurl}}/assets/pngs/img.png)


<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/building_inventory.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/ketan96-m/dataviz/blob/main/deekshitula_shruti_assignment10.ipynb" text="HomeWork10" %}
</div>