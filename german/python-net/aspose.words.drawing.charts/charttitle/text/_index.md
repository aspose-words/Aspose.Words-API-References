---
title: ChartTitle.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "ChartTitle.text property. Gets or sets the text of the chart title"
type: docs
weight: 70
url: /de/python-net/aspose.words.drawing.charts/charttitle/text/
---

## ChartTitle.text property

Gets or sets the text of the chart title.
If ``None`` or empty value is specified, auto generated title will be shown.



```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Remarks

Use [ChartTitle.show](../show/) option if you need to hide the Title.


### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Füge ein Diagramm-Shape mit einem Document Builder ein und rufe sein Diagramm ab.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Verwende die Eigenschaft "Title", um unserem Diagramm einen Titel zu geben, der oben in der Mitte des Diagrammbereichs erscheint.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Setze die Eigenschaft "Show" auf "true", um den Titel sichtbar zu machen.
title.show = True
# Setze die Eigenschaft "Overlay" auf "true", um anderen Diagrammelementen mehr Platz zu geben, indem sie den Titel überlappen dürfen
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

