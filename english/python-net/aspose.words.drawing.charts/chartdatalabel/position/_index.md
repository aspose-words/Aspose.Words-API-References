---
title: ChartDataLabel.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "ChartDataLabel.position property. Gets or sets the position of the data label."
type: docs
weight: 100
url: /python-net/aspose.words.drawing.charts/chartdatalabel/position/
---

## ChartDataLabel.position property

Gets or sets the position of the data label.


```python
@property
def position(self) -> aspose.words.drawing.charts.ChartDataLabelPosition:
    ...

@position.setter
def position(self, value: aspose.words.drawing.charts.ChartDataLabelPosition):
    ...

```

### Remarks

The position can be set for data labels of the following chart series types:

- [ChartSeriesType.BAR](../../chartseriestype/#BAR), [ChartSeriesType.COLUMN](../../chartseriestype/#COLUMN),
[ChartSeriesType.HISTOGRAM](../../chartseriestype/#HISTOGRAM), [ChartSeriesType.PARETO](../../chartseriestype/#PARETO),
[ChartSeriesType.WATERFALL](../../chartseriestype/#WATERFALL); allowed values: [ChartDataLabelPosition.CENTER](../../chartdatalabelposition/#CENTER),
[ChartDataLabelPosition.INSIDE_BASE](../../chartdatalabelposition/#INSIDE_BASE), [ChartDataLabelPosition.INSIDE_END](../../chartdatalabelposition/#INSIDE_END) and
[ChartDataLabelPosition.OUTSIDE_END](../../chartdatalabelposition/#OUTSIDE_END);

- [ChartSeriesType.BAR_STACKED](../../chartseriestype/#BAR_STACKED), [ChartSeriesType.BAR_PERCENT_STACKED](../../chartseriestype/#BAR_PERCENT_STACKED),
[ChartSeriesType.COLUMN_STACKED](../../chartseriestype/#COLUMN_STACKED), [ChartSeriesType.COLUMN_PERCENT_STACKED](../../chartseriestype/#COLUMN_PERCENT_STACKED); allowed
values: [ChartDataLabelPosition.CENTER](../../chartdatalabelposition/#CENTER), [ChartDataLabelPosition.INSIDE_BASE](../../chartdatalabelposition/#INSIDE_BASE)
and [ChartDataLabelPosition.INSIDE_END](../../chartdatalabelposition/#INSIDE_END);

- [ChartSeriesType.BUBBLE](../../chartseriestype/#BUBBLE), [ChartSeriesType.BUBBLE_3D](../../chartseriestype/#BUBBLE_3D),
[ChartSeriesType.LINE](../../chartseriestype/#LINE), [ChartSeriesType.LINE_STACKED](../../chartseriestype/#LINE_STACKED),
[ChartSeriesType.LINE_PERCENT_STACKED](../../chartseriestype/#LINE_PERCENT_STACKED), [ChartSeriesType.SCATTER](../../chartseriestype/#SCATTER),
[ChartSeriesType.STOCK](../../chartseriestype/#STOCK); allowed values: [ChartDataLabelPosition.CENTER](../../chartdatalabelposition/#CENTER),
[ChartDataLabelPosition.LEFT](../../chartdatalabelposition/#LEFT), [ChartDataLabelPosition.RIGHT](../../chartdatalabelposition/#RIGHT),
[ChartDataLabelPosition.ABOVE](../../chartdatalabelposition/#ABOVE) and [ChartDataLabelPosition.BELOW](../../chartdatalabelposition/#BELOW);

- [ChartSeriesType.PIE](../../chartseriestype/#PIE), [ChartSeriesType.PIE_3D](../../chartseriestype/#PIE_3D),
[ChartSeriesType.PIE_OF_BAR](../../chartseriestype/#PIE_OF_BAR), [ChartSeriesType.PIE_OF_PIE](../../chartseriestype/#PIE_OF_PIE); allowed values:
[ChartDataLabelPosition.CENTER](../../chartdatalabelposition/#CENTER), [ChartDataLabelPosition.INSIDE_END](../../chartdatalabelposition/#INSIDE_END),
[ChartDataLabelPosition.OUTSIDE_END](../../chartdatalabelposition/#OUTSIDE_END) and [ChartDataLabelPosition.BEST_FIT](../../chartdatalabelposition/#BEST_FIT);

- [ChartSeriesType.BOX_AND_WHISKER](../../chartseriestype/#BOX_AND_WHISKER); allowed values:
[ChartDataLabelPosition.LEFT](../../chartdatalabelposition/#LEFT), [ChartDataLabelPosition.RIGHT](../../chartdatalabelposition/#RIGHT),
[ChartDataLabelPosition.ABOVE](../../chartdatalabelposition/#ABOVE) and [ChartDataLabelPosition.BELOW](../../chartdatalabelposition/#BELOW).




### Examples

Shows how to set the position of the data label.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert column chart.
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.COLUMN, width=432, height=252)
chart = shape.chart
series_coll = chart.series
# Delete default generated series.
series_coll.clear()
# Add series.
series = series_coll.add(series_name='Series 1', categories=['Category 1', 'Category 2', 'Category 3'], values=[4, 5, 6])
# Show data labels and set font color.
series.has_data_labels = True
data_labels = series.data_labels
data_labels.show_value = True
data_labels.font.color = aspose.pydrawing.Color.white
# Set data label position.
data_labels.position = aw.drawing.charts.ChartDataLabelPosition.INSIDE_BASE
data_labels[0].position = aw.drawing.charts.ChartDataLabelPosition.OUTSIDE_END
data_labels[0].font.color = aspose.pydrawing.Color.dark_red
doc.save(file_name=ARTIFACTS_DIR + 'Charts.LabelPosition.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartDataLabel](../)

