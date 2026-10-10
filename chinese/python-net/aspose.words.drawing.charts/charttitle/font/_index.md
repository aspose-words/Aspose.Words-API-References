---
title: ChartTitle.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ChartTitle.font property. Provides access to the font formatting of the chart title."
type: docs
weight: 10
url: /zh/python-net/aspose.words.drawing.charts/charttitle/font/
---

## ChartTitle.font property

Provides access to the font formatting of the chart title.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 使用文档生成器插入图表形状并获取其图表。
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# 使用 "Title" 属性为我们的图表设置标题，标题显示在图表区域的顶部中心。
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# 将 "Show" 属性设为 "true" 以使标题可见。
title.show = True
# 将 "Overlay" 属性设为 "true"，通过允许它们覆盖标题，为其他图表元素提供更多空间
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

