---
title: "Malaria Analysis"
date: 2021-10-01T15:39:23-04:00
draft: False
---
## Background
Malaria may not be a very familiar disease to people in those more developed areas of the globe. However, at places where the climate is suitable for mosquitoes to reproduce, public health practices are most advanced and population density is high, Malaria has been a leading factor of death cases. The most horrific part about this disease that, it only takes on mosquito bite to be infected. How has the world tackled this life-threatening diseas, and what countires have made impressive progress? We will find out from visualizing three sets of Malaria data using Altair. 

## Data 

## Tool

## Visualization and insights

```python
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

## Visualization and insights
{{< rawhtml >}}
  <p class="speshal-fancy-custom">
    This is <strong>raw HTML</strong>, inside Markdown.
  </p>
{{< /rawhtml >}}

## Test
{{< rawhtml >}}
<head>
  <style>
    .error {
        color: red;
    }
  </style>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@4.8.1"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@6"></script>
</head>
<body>
  <div id="vis"></div>
  <script>
    (function(vegaEmbed) {
      var spec = {"config": {"view": {"continuousWidth": 400, "continuousHeight": 300}, "title": {"anchor": "middle", "color": "Black", "fontSize": 15}}, "layer": [{"mark": "circle", "encoding": {"color": {"type": "nominal", "field": "Entity", "legend": {"title": "Country"}}, "opacity": {"value": 0}, "tooltip": [{"type": "nominal", "field": "Entity"}, {"type": "quantitative", "field": "Year"}, {"type": "quantitative", "field": "Incidents per 100,000 at risk"}], "x": {"type": "quantitative", "field": "Year", "scale": {"zero": false}}, "y": {"type": "quantitative", "aggregate": "sum", "field": "Incidents per 100,000 at risk", "title": "Incident per 1000 at risk"}}, "selection": {"selector021": {"type": "single", "on": "mouseover", "fields": ["Entity"], "nearest": true}}, "width": 500}, {"mark": "line", "encoding": {"color": {"type": "nominal", "field": "Entity", "legend": {"title": "Country"}}, "size": {"condition": {"value": 1, "selection": {"not": "selector021"}}, "value": 6}, "tooltip": [{"type": "nominal", "field": "Entity"}, {"type": "quantitative", "field": "Year"}, {"type": "quantitative", "field": "Incidents per 100,000 at risk"}], "x": {"type": "quantitative", "field": "Year", "scale": {"zero": false}}, "y": {"type": "quantitative", "aggregate": "sum", "field": "Incidents per 100,000 at risk", "title": "Incident per 1000 at risk"}}}], "data": {"name": "data-05ea87fd3d0bde342df4f77fd983953a"}, "title": "Incidents per 1000 population at risk in Top 10 Malaria-Hard-Hit Countries", "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json", "datasets": {"data-05ea87fd3d0bde342df4f77fd983953a": [{"Entity": "Burkina Faso", "Code": "BFA", "Year": 2000, "Incidents per 100,000 at risk": 621.6}, {"Entity": "Burkina Faso", "Code": "BFA", "Year": 2005, "Incidents per 100,000 at risk": 549.8}, {"Entity": "Burkina Faso", "Code": "BFA", "Year": 2010, "Incidents per 100,000 at risk": 601.4}, {"Entity": "Burkina Faso", "Code": "BFA", "Year": 2015, "Incidents per 100,000 at risk": 389.2}, {"Entity": "Burundi", "Code": "BDI", "Year": 2000, "Incidents per 100,000 at risk": 418.8}, {"Entity": "Burundi", "Code": "BDI", "Year": 2005, "Incidents per 100,000 at risk": 273.3}, {"Entity": "Burundi", "Code": "BDI", "Year": 2010, "Incidents per 100,000 at risk": 198.2}, {"Entity": "Burundi", "Code": "BDI", "Year": 2015, "Incidents per 100,000 at risk": 126.3}, {"Entity": "Democratic Republic of Congo", "Code": "COD", "Year": 2000, "Incidents per 100,000 at risk": 508.5}, {"Entity": "Democratic Republic of Congo", "Code": "COD", "Year": 2005, "Incidents per 100,000 at risk": 524.9}, {"Entity": "Democratic Republic of Congo", "Code": "COD", "Year": 2010, "Incidents per 100,000 at risk": 427.2}, {"Entity": "Democratic Republic of Congo", "Code": "COD", "Year": 2015, "Incidents per 100,000 at risk": 246.0}, {"Entity": "Malawi", "Code": "MWI", "Year": 2000, "Incidents per 100,000 at risk": 432.0}, {"Entity": "Malawi", "Code": "MWI", "Year": 2005, "Incidents per 100,000 at risk": 321.2}, {"Entity": "Malawi", "Code": "MWI", "Year": 2010, "Incidents per 100,000 at risk": 419.5}, {"Entity": "Malawi", "Code": "MWI", "Year": 2015, "Incidents per 100,000 at risk": 188.8}, {"Entity": "Mali", "Code": "MLI", "Year": 2000, "Incidents per 100,000 at risk": 476.8}, {"Entity": "Mali", "Code": "MLI", "Year": 2005, "Incidents per 100,000 at risk": 498.2}, {"Entity": "Mali", "Code": "MLI", "Year": 2010, "Incidents per 100,000 at risk": 364.7}, {"Entity": "Mali", "Code": "MLI", "Year": 2015, "Incidents per 100,000 at risk": 448.6}, {"Entity": "Mozambique", "Code": "MOZ", "Year": 2000, "Incidents per 100,000 at risk": 515.6}, {"Entity": "Mozambique", "Code": "MOZ", "Year": 2005, "Incidents per 100,000 at risk": 442.3}, {"Entity": "Mozambique", "Code": "MOZ", "Year": 2010, "Incidents per 100,000 at risk": 383.3}, {"Entity": "Mozambique", "Code": "MOZ", "Year": 2015, "Incidents per 100,000 at risk": 297.7}, {"Entity": "Niger", "Code": "NER", "Year": 2000, "Incidents per 100,000 at risk": 443.6}, {"Entity": "Niger", "Code": "NER", "Year": 2005, "Incidents per 100,000 at risk": 463.1}, {"Entity": "Niger", "Code": "NER", "Year": 2010, "Incidents per 100,000 at risk": 499.9}, {"Entity": "Niger", "Code": "NER", "Year": 2015, "Incidents per 100,000 at risk": 356.5}, {"Entity": "Nigeria", "Code": "NGA", "Year": 2000, "Incidents per 100,000 at risk": 497.8}, {"Entity": "Nigeria", "Code": "NGA", "Year": 2005, "Incidents per 100,000 at risk": 482.6}, {"Entity": "Nigeria", "Code": "NGA", "Year": 2010, "Incidents per 100,000 at risk": 416.3}, {"Entity": "Nigeria", "Code": "NGA", "Year": 2015, "Incidents per 100,000 at risk": 380.8}, {"Entity": "Sierra Leone", "Code": "SLE", "Year": 2000, "Incidents per 100,000 at risk": 486.0}, {"Entity": "Sierra Leone", "Code": "SLE", "Year": 2005, "Incidents per 100,000 at risk": 468.5}, {"Entity": "Sierra Leone", "Code": "SLE", "Year": 2010, "Incidents per 100,000 at risk": 482.0}, {"Entity": "Sierra Leone", "Code": "SLE", "Year": 2015, "Incidents per 100,000 at risk": 302.8}, {"Entity": "Uganda", "Code": "UGA", "Year": 2000, "Incidents per 100,000 at risk": 516.8}, {"Entity": "Uganda", "Code": "UGA", "Year": 2005, "Incidents per 100,000 at risk": 477.6}, {"Entity": "Uganda", "Code": "UGA", "Year": 2010, "Incidents per 100,000 at risk": 429.1}, {"Entity": "Uganda", "Code": "UGA", "Year": 2015, "Incidents per 100,000 at risk": 218.3}]}};
      var embedOpt = {"mode": "vega-lite"};

      function showError(el, error){
          el.innerHTML = ('<div class="error" style="color:red;">'
                          + '<p>JavaScript Error: ' + error.message + '</p>'
                          + "<p>This usually means there's a typo in your chart specification. "
                          + "See the javascript console for the full traceback.</p>"
                          + '</div>');
          throw error;
      }
      const el = document.getElementById('vis');
      vegaEmbed("#vis", spec, embedOpt)
        .catch(error => showError(el, error));
    })(vegaEmbed);

  </script>
</body>
{{< /rawhtml >}}