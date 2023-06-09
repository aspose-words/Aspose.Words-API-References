---
title: ChartYValue.from_double method
linktitle: from_double method
articleTitle: from_double method
second_title: Aspose.Words for Python
description: "ChartYValue.from_double method. Creates a [ChartYValue](../) instance of the [ChartYValueType.DOUBLE](../../chartyvaluetype/#DOUBLE) type."
type: docs
weight: 60
url: /python-net/aspose.words.drawing.charts/chartyvalue/from_double/
---

## from_double(value) {#float}

Creates a [ChartYValue](../) instance of the [ChartYValueType.DOUBLE](../../chartyvaluetype/#DOUBLE) type.



```python
def from_double(self, value: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | float |  |

### Examples

Shows how to populate chart series with data.

```python
doc = Document()
builder = DocumentBuilder()

shape = builder.insert_chart(ChartType.COLUMN, 432, 252)
chart = shape.chart
series1 = chart.series[0]

# Clear X and Y values of the first series.
series1.clear_values()

# Populate the series with data.
series1.add(ChartXValue.from_double(3), ChartYValue.from_double(10))
series1.add(ChartXValue.from_double(5), ChartYValue.from_double(5))
series1.add(ChartXValue.from_double(7), ChartYValue.from_double(11))
series1.add(ChartXValue.from_double(9), ChartYValue.from_double(17))

series2 = chart.series[1]

# Clear X and Y values of the second series.
series2.clear_values();

# Populate the series with data.
series2.add(ChartXValue.from_double(2), ChartYValue.from_double(4))
series2.add(ChartXValue.from_double(4), ChartYValue.from_double(7))
series2.add(ChartXValue.from_double(6), ChartYValue.from_double(14))
series2.add(ChartXValue.from_double(8), ChartYValue.from_double(7))

doc.save(ARTIFACTS_DIR + "Charts.PopulateChartWithData.docx");
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartYValue](../)

