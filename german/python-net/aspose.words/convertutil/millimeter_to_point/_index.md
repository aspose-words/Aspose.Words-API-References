---
title: ConvertUtil.millimeter_to_point method
linktitle: millimeter_to_point method
articleTitle: millimeter_to_point method
second_title: Aspose.Words for Python
description: "ConvertUtil.millimeter_to_point method. Converts millimeters to points."
type: docs
weight: 20
url: /de/python-net/aspose.words/convertutil/millimeter_to_point/
---

## millimeter_to_point(millimeters) {#float}

Converts millimeters to points.


```python
def millimeter_to_point(self, millimeters: float):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | float | The value to convert. |

### Remarks

1 inch equals 25.4 millimeters. 1 inch equals 72 points.


### Examples

Shows how to specify page properties in millimeters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Der "Page Setup" eines Abschnitts definiert die Größe der Seitenränder in Punkten.
# Wir können auch die Klasse "ConvertUtil" verwenden, um eine vertrautere Maßeinheit zu nutzen,
# wie Millimeter beim Definieren von Grenzen.
page_setup = builder.page_setup
page_setup.top_margin = aw.ConvertUtil.millimeter_to_point(30)
page_setup.bottom_margin = aw.ConvertUtil.millimeter_to_point(50)
page_setup.left_margin = aw.ConvertUtil.millimeter_to_point(80)
page_setup.right_margin = aw.ConvertUtil.millimeter_to_point(40)
# Ein Zentimeter entspricht ungefähr 28,3 Punkten.
self.assertAlmostEqual(28.34, aw.ConvertUtil.millimeter_to_point(10), delta=0.01)
# Füge Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder.writeln(f'This Text is {page_setup.left_margin} points from the left, ' + f'{page_setup.right_margin} points from the right, ' + f'{page_setup.top_margin} points from the top, ' + f'and {page_setup.bottom_margin} points from the bottom of the page.')
doc.save(file_name=ARTIFACTS_DIR + 'UtilityClasses.PointsAndMillimeters.docx')
```

### See Also

* module [aspose.words](../../)
* class [ConvertUtil](../)

