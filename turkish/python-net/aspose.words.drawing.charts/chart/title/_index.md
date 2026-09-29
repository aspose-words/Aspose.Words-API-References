---
title: Chart.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "Chart.title property. Provides access to the chart title properties."
type: docs
weight: 120
url: /tr/python-net/aspose.words.drawing.charts/chart/title/
---

## Chart.title property

Provides access to the chart title properties.


```python
@property
def title(self) -> aspose.words.drawing.charts.ChartTitle:
    ...

```

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Bir belge oluşturucu ile bir grafik şekli ekle ve grafiğini al.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# \"Title\" özelliğini kullanarak grafiğimize bir başlık ver, bu başlık grafik alanının üst orta kısmında görünür.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# \"Show\" özelliğini \"true\" olarak ayarla ve başlığı görünür yap.
title.show = True
# \"Overlay\" özelliğini \"true\" olarak ayarla, başlığın üzerine gelmelerine izin vererek diğer grafik öğelerine daha fazla alan tanı.
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [Chart](../)

