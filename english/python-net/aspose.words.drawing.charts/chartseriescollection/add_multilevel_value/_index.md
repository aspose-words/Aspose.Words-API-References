---
title: ChartSeriesCollection.add_multilevel_value method
linktitle: add_multilevel_value method
articleTitle: add_multilevel_value method
second_title: Aspose.Words for Python
description: "ChartSeriesCollection.add_multilevel_value method. Adds new [ChartSeries](../../chartseries/) to this collection"
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartseriescollection/add_multilevel_value/
---

## add_multilevel_value(series_name, categories, values) {#str_chartmultilevelvaluelist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series that have multi-level data categories.



```python
def add_multilevel_value(self, series_name: str, categories: List[aspose.words.drawing.charts.ChartMultilevelValue], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| categories | List[[ChartMultilevelValue](../../chartmultilevelvalue/)] |  |
| values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


### Examples

Shows how to create treemap chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a Treemap chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.TREEMAP, width=450, height=280)
chart = shape.chart
chart.title.text = 'World Population'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add_multilevel_value(series_name='Population by Region', categories=[aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='China'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='India'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Indonesia'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Pakistan'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Bangladesh'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Japan'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Philippines'), aw.drawing.charts.ChartMultilevelValue(level1='Asia', level2='Other'), aw.drawing.charts.ChartMultilevelValue(level1='Africa', level2='Nigeria'), aw.drawing.charts.ChartMultilevelValue(level1='Africa', level2='Ethiopia'), aw.drawing.charts.ChartMultilevelValue(level1='Africa', level2='Egypt'), aw.drawing.charts.ChartMultilevelValue(level1='Africa', level2='Other'), aw.drawing.charts.ChartMultilevelValue(level1='Europe', level2='Russia'), aw.drawing.charts.ChartMultilevelValue(level1='Europe', level2='Germany'), aw.drawing.charts.ChartMultilevelValue(level1='Europe', level2='Other'), aw.drawing.charts.ChartMultilevelValue(level1='Latin America', level2='Brazil'), aw.drawing.charts.ChartMultilevelValue(level1='Latin America', level2='Mexico'), aw.drawing.charts.ChartMultilevelValue(level1='Latin America', level2='Other'), aw.drawing.charts.ChartMultilevelValue(level1='Northern America', level2='United States'), aw.drawing.charts.ChartMultilevelValue(level1='Northern America', level2='Other'), aw.drawing.charts.ChartMultilevelValue(level1='Oceania')], values=[1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000, 223800000, 107334000, 105914499, 903000000, 146150789, 84607016, 516000000, 203080756, 129713690, 310000000, 335893238, 35000000, 42000000])
# Show data labels.
series.has_data_labels = True
series.data_labels.show_value = True
series.data_labels.show_category_name = True
decimal_separator = locale.localeconv()['decimal_point']
series.data_labels.number_format.format_code = f"0{decimal_separator}0%"
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Treemap.docx')
```

Shows how to create sunburst chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a Sunburst chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.SUNBURST, width=450, height=450)
chart = shape.chart
chart.title.text = 'Sales'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add_multilevel_value(series_name='Sales', categories=[aw.drawing.charts.ChartMultilevelValue(level1='Sales - Europe', level2='UK', level3='London Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Europe', level2='UK', level3='Liverpool Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Europe', level2='UK', level3='Manchester Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Europe', level2='France', level3='Paris Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Europe', level2='France', level3='Lyon Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='USA', level3='Denver Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='USA', level3='Seattle Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='USA', level3='Detroit Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='USA', level3='Houston Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='Canada', level3='Toronto Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - NA', level2='Canada', level3='Montreal Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Oceania', level2='Australia', level3='Sydney Dep.'), aw.drawing.charts.ChartMultilevelValue(level1='Sales - Oceania', level2='New Zealand', level3='Auckland Dep.')], values=[1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694])
# Show data labels.
series.has_data_labels = True
series.data_labels.show_value = False
series.data_labels.show_category_name = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Sunburst.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

