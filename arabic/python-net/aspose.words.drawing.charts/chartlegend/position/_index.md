---
title: ChartLegend.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "ChartLegend.position property. Specifies the position of the legend on a chart."
type: docs
weight: 50
url: /ar/python-net/aspose.words.drawing.charts/chartlegend/position/
---

## ChartLegend.position property

Specifies the position of the legend on a chart.


```python
@property
def position(self) -> aspose.words.drawing.charts.LegendPosition:
    ...

@position.setter
def position(self, value: aspose.words.drawing.charts.LegendPosition):
    ...

```

### Remarks

The default value is [LegendPosition.RIGHT](../../legendposition/#RIGHT) for pre-Word 2016 charts and
[LegendPosition.TOP](../../legendposition/#TOP) for Word 2016 charts.



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
# انقل وسيلة إيضاح المخطط إلى الزاوية العليا اليمنى.
legend = chart.legend
legend.position = aw.drawing.charts.LegendPosition.TOP_RIGHT
# امنح عناصر المخطط الأخرى، مثل الرسم البياني، مساحة أكبر بالسماح لها بالتداخل مع وسيلة الإيضاح.
legend.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartLegend.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartLegend](../)

