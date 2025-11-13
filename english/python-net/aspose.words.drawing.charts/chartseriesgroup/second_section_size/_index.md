---
title: ChartSeriesGroup.second_section_size property
linktitle: second_section_size property
articleTitle: second_section_size property
second_title: Aspose.Words for Python
description: "ChartSeriesGroup.second_section_size property. Gets or sets the size of the pie chart secondary section as a percentage."
type: docs
weight: 90
url: /python-net/aspose.words.drawing.charts/chartseriesgroup/second_section_size/
---

## ChartSeriesGroup.second_section_size property

Gets or sets the size of the pie chart secondary section as a percentage.


```python
@property
def second_section_size(self) -> int:
    ...

@second_section_size.setter
def second_section_size(self, value: int):
    ...

```

### Remarks

Applies to series groups of the [ChartSeriesType.PIE_OF_PIE](../../chartseriestype/#PIE_OF_PIE) and
[ChartSeriesType.PIE_OF_BAR](../../chartseriestype/#PIE_OF_BAR) types.

The range of acceptable values is from 5 to 200 inclusive. The default value is 75.




### Examples

Shows how to create and format pie of Pie chart.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.PIE_OF_PIE, width=440, height=300)
chart = shape.chart
# Delete the default generated series.
chart.series.clear()
categories = ['Category 1', 'Category 2', 'Category 3', 'Category 4']
chart.series.add1(series_name='Series 1', categories=categories, values=[11, 8, 4, 3])
# Format the Pie of Pie chart.
series_group = chart.series_groups[0]
series_group.gap_width = 10
series_group.second_section_size = 77
doc.save(file_name=ARTIFACTS_DIR + 'Charts.PieOfPieChart.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartSeriesGroup](../)

