---
title: ShapeBase.fill property
linktitle: fill property
articleTitle: fill property
second_title: Aspose.Words for Python
description: "ShapeBase.fill property. Gets fill formatting for the shape."
type: docs
weight: 170
url: /de/python-net/aspose.words.drawing/shapebase/fill/
---

## ShapeBase.fill property

Gets fill formatting for the shape.


```python
@property
def fill(self) -> aspose.words.drawing.Fill:
    ...

```

### Examples

Shows how to fill a shape with a solid color.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Schreiben Sie etwas Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Verwenden Sie die "StrokeColor"-Eigenschaft, um die Farbe der Kontur der Form festzulegen.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Verwenden Sie die "FillColor"-Eigenschaft, um die Farbe des Innenbereichs der Form festzulegen.
shape.fill_color = aspose.pydrawing.Color.light_blue
# Die "Opacity"-Eigenschaft bestimmt, wie transparent die Farbe auf einer Skala von 0 bis 1 ist,
# wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
# Die Füllung der Form ist standardmäßig vollständig undurchsichtig, sodass wir den Text, über dem sich die Form befindet, nicht sehen können.
self.assertEqual(1, shape.fill.opacity)
# Setzen Sie die Opazität der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den darunter liegenden Text sehen können.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

