---
title: ChartLegend.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Python
description: "ChartLegend.overlay property. Determines whether other chart elements shall be allowed to overlap legend"
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing.charts/chartlegend/overlay/
---

## ChartLegend.overlay property

Determines whether other chart elements shall be allowed to overlap legend.
Default value is ``False``.



```python
@property
def overlay(self) -> bool:
    ...

@overlay.setter
def overlay(self, value: bool):
    ...

```

### Examples

Shows how to edit the appearance of a chart's legend.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.LINE, width=450, height=300)
chart = shape.chart
self.assertEqual(3, chart.series.count)
self.assertEqual('Series 1', chart.series[0].name)
self.assertEqual('Series 2', chart.series[1].name)
self.assertEqual('Series 3', chart.series[2].name)
# 将图表的图例移动到右上角。
legend = chart.legend
legend.position = aw.drawing.charts.LegendPosition.TOP_RIGHT
# 通过允许其他图表元素（如图形）覆盖图例，为它们提供更多空间。
legend.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartLegend.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegend](../)

