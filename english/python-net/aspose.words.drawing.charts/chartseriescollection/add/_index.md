---
title: ChartSeriesCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.charts.ChartSeriesCollection.add method"
type: docs
weight: 30
url: /python-net/aspose.words.drawing.charts/chartseriescollection/add/
---

## add(series_name, categories, values) {#str_strlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bar, Column, Line and Surface charts.



```python
def add(self, series_name: str, categories: List[str], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| categories | List[str] |  |
| values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, x_values, y_values) {#str_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Scatter charts.



```python
def add(self, series_name: str, x_values: List[float], y_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, dates, values) {#str_datetimelist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Area, Radar and Stock charts.



```python
def add(self, series_name: str, dates: List[datetime.datetime], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| dates | List[datetime.datetime] |  |
| values | List[float] |  |

## add(series_name, x_values, y_values, bubble_sizes) {#str_floatlist_floatlist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to any type of Bubble charts.



```python
def add(self, series_name: str, x_values: List[float], y_values: List[float], bubble_sizes: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |
| y_values | List[float] |  |
| bubble_sizes | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, categories, values) {#str_chartmultilevelvaluelist_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series that have multi-level data categories.



```python
def add(self, series_name: str, categories: List[aspose.words.drawing.charts.ChartMultilevelValue], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| categories | List[[ChartMultilevelValue](../../chartmultilevelvalue/)] |  |
| values | List[float] |  |

### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, x_values) {#str_floatlist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Histogram charts.



```python
def add(self, series_name: str, x_values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| x_values | List[float] |  |

### Remarks

For chart types other than Histogram, this method adds a series with empty Y values.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## add(series_name, categories, values, is_subtotal) {#str_strlist_floatlist_boollist}

Adds new [ChartSeries](../../chartseries/) to this collection.
Use this method to add series to Waterfall charts.



```python
def add(self, series_name: str, categories: List[str], values: List[float], is_subtotal: List[bool]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str | A name of the series to be added. |
| categories | List[str] | Category names for the X axis. |
| values | List[float] | Y-axis values. |
| is_subtotal | List[bool] | Values indicating whether the corresponding Y value is a subtotal. |

### Remarks

For chart types other than Waterfall, *isSubtotal* values are ignored.


### Returns

Recently added [ChartSeries](../../chartseries/) object.


## Examples

Shows how to create pareto chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Pareto chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PARETO, width=450, height=450)
chart = shape.chart
chart.title.text = 'Best-Selling Car'
# Delete default generated series.
chart.series.clear()
# Add a series.
chart.series.add(series_name='Best-Selling Car', categories=['Tesla Model Y', 'Toyota Corolla', 'Toyota RAV4', 'Ford F-Series', 'Honda CR-V'], values=[1.43, 0.91, 1.17, 0.98, 0.85])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Pareto.docx')
```

Shows how to create box and whisker chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Box & Whisker chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BOX_AND_WHISKER, width=450, height=450)
chart = shape.chart
chart.title.text = 'Points by Years'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add(series_name='Points by Years', categories=['WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'WC', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NR', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA', 'NA'], values=[91, 80, 100, 77, 90, 104, 105, 118, 120, 101, 114, 107, 110, 60, 79, 78, 77, 102, 101, 113, 94, 93, 84, 71, 80, 103, 80, 94, 100, 101])
# Show data labels.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.BoxAndWhisker.docx')
```

Shows how to create an appropriate type of chart series for a graph type.

```python
def chart_series_collection():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    # There are several ways of populating a chart's series collection.
    # Different series schemas are intended for different chart types.
    # 1 -  Column chart with columns grouped and banded along the X-axis by category:
    chart = append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)
    categories = ['Category 1', 'Category 2', 'Category 3']
    # Insert two series of decimal values containing a value for each respective category.
    # This column chart will have three groups, each with two columns.
    chart.series.add('Series 1', categories, [76.6, 82.1, 91.6])
    chart.series.add('Series 2', categories, [64.2, 79.5, 94.0])
    # Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
    # 2 -  Area chart with dates distributed along the X-axis:
    chart = append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)
    dates = [date(2014, 3, 31), date(2017, 1, 23), date(2017, 6, 18), date(2019, 11, 22), date(2020, 9, 7)]
    # Insert a series with a decimal value for each respective date.
    # The dates will be distributed along a linear X-axis,
    # and the values added to this series will create data points.
    chart.series.add('Series 1', dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])
    self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
    # 3 -  2D scatter plot:
    chart = append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)
    # Each series will need two decimal arrays of equal length.
    # The first array contains X-values, and the second contains corresponding Y-values
    # of data points on the chart's graph.
    chart.series.add('Series 1', x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6], y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
    chart.series.add('Series 2', x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3], y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)
    # 4 -  Bubble chart:
    chart = append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)
    # Each series will need three decimal arrays of equal length.
    # The first array contains X-values, the second contains corresponding Y-values,
    # and the third contains diameters for each of the graph's data points.
    chart.series.add('Series 1', [1.1, 5.0, 9.8], [1.2, 4.9, 9.9], [2.0, 4.0, 8.0])
    doc.save(ARTIFACTS_DIR + 'Charts.chart_series_collection.docx')

def append_chart(builder: aw.DocumentBuilder, chart_type: aw.drawing.charts.ChartType, width: float, height: float) -> aw.drawing.charts.Chart:
    """Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data."""
    chart_shape = builder.insert_chart(chart_type, width, height)
    chart = chart_shape.chart
    chart.series.clear()
    return chart
```

Shows how to create funnel chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a Funnel chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.FUNNEL, width=450, height=450)
chart = shape.chart
chart.title.text = 'Population by Age Group'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add(series_name='Population by Age Group', categories=['0-9', '10-19', '20-29', '30-39', '40-49', '50-59', '60-69', '70-79', '80-89', '90-'], values=[0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007])
# Show data labels.
series.has_data_labels = True
decimal_separator = locale.localeconv()['decimal_point']
series.data_labels.number_format.format_code = f'0{decimal_separator}0%'
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Funnel.docx')
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

Shows how to create histogram chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Histogram chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.HISTOGRAM, width=450, height=450)
chart = shape.chart
chart.title.text = 'Avg Temperature since 1991'
# Delete default generated series.
chart.series.clear()
# Add a series.
chart.series.add(series_name='Avg Temperature', x_values=[51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52, 55, 52.1, 53.4, 53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7, 56.3, 55.9, 55.6])
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Histogram.docx')
```

Shows how to create waterfall chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a Waterfall chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.WATERFALL, width=450, height=450)
chart = shape.chart
chart.title.text = 'New Zealand GDP'
# Delete default generated series.
chart.series.clear()
# Add a series.
series = chart.series.add(series_name='New Zealand GDP', categories=['2018', '2019 growth', '2020 growth', '2020', '2021 growth', '2022 growth', '2022'], values=[100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62], is_subtotal=[True, False, False, True, False, False, True])
# Show data labels.
series.has_data_labels = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.Waterfall.docx')
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

