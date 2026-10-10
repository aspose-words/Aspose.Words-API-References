---
title: ShapeBase.fill property
linktitle: fill property
articleTitle: fill property
second_title: Aspose.Words for Python
description: "ShapeBase.fill property. Gets fill formatting for the shape."
type: docs
weight: 170
url: /it/python-net/aspose.words.drawing/shapebase/fill/
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
# Scrivi del testo, quindi coprilo con una forma fluttuante.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Usa la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Usa la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape.fill_color = aspose.pydrawing.Color.light_blue
# La proprietà "Opacity" determina quanto è trasparente il colore su una scala da 0 a 1,
# con 1 completamente opaco e 0 invisibile.
# Il riempimento della forma è per impostazione predefinita completamente opaco, quindi non possiamo vedere il testo su cui questa forma è sovrapposta.
self.assertEqual(1, shape.fill.opacity)
# Imposta l'opacità del colore di riempimento della forma a un valore più basso così da poter vedere il testo sottostante.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

