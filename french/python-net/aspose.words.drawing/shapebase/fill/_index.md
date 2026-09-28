---
title: ShapeBase.fill property
linktitle: fill property
articleTitle: fill property
second_title: Aspose.Words for Python
description: "ShapeBase.fill property. Gets fill formatting for the shape."
type: docs
weight: 170
url: /fr/python-net/aspose.words.drawing/shapebase/fill/
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
# Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.font.size = 32
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CLOUD_CALLOUT, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=25, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=25, width=250, height=150, wrap_type=aw.drawing.WrapType.NONE)
# Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape.stroke_color = aspose.pydrawing.Color.cadet_blue
# Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape.fill_color = aspose.pydrawing.Color.light_blue
# La propriété "Opacity" détermine le degré de transparence de la couleur sur une échelle de 0 à 1,
# 1 étant totalement opaque, et 0 étant invisible.
# Le remplissage de la forme est, par défaut, totalement opaque, donc nous ne pouvons pas voir le texte sur lequel cette forme se trouve.
self.assertEqual(1, shape.fill.opacity)
# Réglez l'opacité de la couleur de remplissage de la forme à une valeur plus basse afin de pouvoir voir le texte en dessous.
shape.fill.opacity = 0.3
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Fill.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

