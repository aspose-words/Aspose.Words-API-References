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
def add(self, series_name: str, dates: List[datetime], values: List[float]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| series_name | str |  |
| dates | List[datetime] |  |
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


## Examples

Shows how to create an appropriate type of chart series for a graph type.

```python
def test_chart_series_collection(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # There are several ways of populating a chart's series collection.
    # Different series schemas are intended for different chart types.
    # 1 -  Column chart with columns grouped and banded along the X-axis by category:
    chart = self.append_chart(builder, aw.drawing.charts.ChartType.COLUMN, 500, 300)

    categories = ["Category 1", "Category 2", "Category 3"]

    # Insert two series of decimal values containing a value for each respective category.
    # This column chart will have three groups, each with two columns.
    chart.series.add("Series 1", categories, [76.6, 82.1, 91.6])
    chart.series.add("Series 2", categories, [64.2, 79.5, 94.0])

    # Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)

    # 2 -  Area chart with dates distributed along the X-axis:
    chart = self.append_chart(builder, aw.drawing.charts.ChartType.AREA, 500, 300)

    dates = [
        date(2014, 3, 31),
        date(2017, 1, 23),
        date(2017, 6, 18),
        date(2019, 11, 22),
        date(2020, 9, 7)
        ]

    # Insert a series with a decimal value for each respective date.
    # The dates will be distributed along a linear X-axis,
    # and the values added to this series will create data points.
    chart.series.add("Series 1", dates=dates, values=[15.8, 21.5, 22.9, 28.7, 33.1])

    self.assertEqual(aw.drawing.charts.ChartAxisType.CATEGORY, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)

    # 3 -  2D scatter plot:
    chart = self.append_chart(builder, aw.drawing.charts.ChartType.SCATTER, 500, 300)

    # Each series will need two decimal arrays of equal length.
    # The first array contains X-values, and the second contains corresponding Y-values
    # of data points on the chart's graph.
    chart.series.add("Series 1",
        x_values=[3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6],
        y_values=[3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9])
    chart.series.add("Series 2",
        x_values=[2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3],
        y_values=[7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6])

    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_x.type)
    self.assertEqual(aw.drawing.charts.ChartAxisType.VALUE, chart.axis_y.type)

    # 4 -  Bubble chart:
    chart = self.append_chart(builder, aw.drawing.charts.ChartType.BUBBLE, 500, 300)

    # Each series will need three decimal arrays of equal length.
    # The first array contains X-values, the second contains corresponding Y-values,
    # and the third contains diameters for each of the graph's data points.
    chart.series.add("Series 1",
        [1.1, 5.0, 9.8],
        [1.2, 4.9, 9.9],
        [2.0, 4.0, 8.0])

    doc.save(ARTIFACTS_DIR + "Charts.chart_series_collection.docx")

def append_chart(self, builder: aw.DocumentBuilder,
                 chart_type: aw.drawing.charts.ChartType,
                 width: float, height: float) -> aw.drawing.charts.Chart:
    """Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data."""

    chart_shape = builder.insert_chart(chart_type, width, height)
    chart = chart_shape.chart
    chart.series.clear()

    return chart
```

## See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesCollection](../)

