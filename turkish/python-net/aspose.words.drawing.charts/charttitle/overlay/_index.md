---
title: ChartTitle.overlay property
linktitle: overlay property
articleTitle: overlay property
second_title: Aspose.Words for Python
description: "ChartTitle.overlay property. Determines whether other chart elements shall be allowed to overlap title"
type: docs
weight: 40
url: /tr/python-net/aspose.words.drawing.charts/charttitle/overlay/
---

## ChartTitle.overlay property

Determines whether other chart elements shall be allowed to overlap title.
By default overlay is ``False``.



```python
@property
def overlay(self) -> bool:
    ...

@overlay.setter
def overlay(self, value: bool):
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
* class [ChartTitle](../)

