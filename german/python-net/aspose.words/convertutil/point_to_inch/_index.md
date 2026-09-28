---
title: ConvertUtil.point_to_inch method
linktitle: point_to_inch method
articleTitle: point_to_inch method
second_title: Aspose.Words for Python
description: "ConvertUtil.point_to_inch method. Converts points to inches."
type: docs
weight: 50
url: /de/python-net/aspose.words/convertutil/point_to_inch/
---

## point_to_inch(points) {#float}

Converts points to inches.


```python
def point_to_inch(self, points: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| points | float | The value to convert. |

### Remarks

1 inch equals 72 points.


### Examples

Shows how to specify page properties in inches.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Der "Page Setup" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
# Wir können auch die Klasse "ConvertUtil" verwenden, um eine vertrautere Maßeinheit zu nutzen,
# wie Zoll beim Definieren von Grenzen.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.inch_to_point(1)
page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(2)
page_setup.left_margin = aw.ConvertUtil.inch_to_point(2.5)
page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
# Ein Zoll entspricht 72 Punkten.
self.assertEqual(72, aw.ConvertUtil.inch_to_point(1))
self.assertEqual(1, aw.ConvertUtil.point_to_inch(72))
# Füge Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder.writeln(f'This Text is {page_setup.left_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.left_margin)} inches from the left, ' + f'{page_setup.right_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.right_margin)} inches from the right, ' + f'{page_setup.top_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.top_margin)} inches from the top, ' + f'and {page_setup.bottom_margin} points/{aw.ConvertUtil.point_to_inch(page_setup.bottom_margin)} inches from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndInches.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

