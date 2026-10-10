---
title: ChartTitle.show property
linktitle: show property
articleTitle: show property
second_title: Aspose.Words for Python
description: "ChartTitle.show property. Determines whether the title shall be shown for this chart"
type: docs
weight: 60
url: /ru/python-net/aspose.words.drawing.charts/charttitle/show/
---

## ChartTitle.show property

Determines whether the title shall be shown for this chart.
Default value is ``True``.



```python
@property
def show(self) -> bool:
    ...

@show.setter
def show(self, value: bool):
    ...

```

### Examples

Shows how to insert a chart and set a title.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте форму диаграммы с помощью Document Builder и получите её диаграмму.
chart_shape = builder.insert_chart(chart_type=aw.drawing.charts.ChartType.BAR, width=400, height=300)
chart = chart_shape.chart
# Используйте свойство \"Title\", чтобы задать нашей диаграмме заголовок, который отображается в верхнем центре области диаграммы.
title = chart.title
title.text = 'My Chart'
title.font.size = 15
title.font.color = aspose.pydrawing.Color.blue
# Установите свойство \"Show\" в \"true\", чтобы сделать заголовок видимым.
title.show = True
# Установите свойство \"Overlay\" в \"true\", чтобы дать другим элементам диаграммы больше места, позволяя им перекрывать заголовок
title.overlay = True
doc.save(file_name=ARTIFACTS_DIR + 'Charts.ChartTitle.docx')
```

### See Also

* module [aspose.words.drawing.charts](../../)
* class [ChartTitle](../)

