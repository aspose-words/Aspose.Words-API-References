---
title: Stroke.on property
linktitle: on property
articleTitle: on property
second_title: Aspose.Words for Python
description: "Stroke.on property. Defines whether the path will be stroked."
type: docs
weight: 190
url: /es/python-net/aspose.words.drawing/stroke/on/
---

## Stroke.on property

Defines whether the path will be stroked.


```python
@property
def on(self) -> bool:
    ...

@on.setter
def on(self, value: bool):
    ...

```

### Remarks

The default value for a [Shape](../../shape/) is ``True``.




### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
# Las formas básicas, como el rectángulo, tienen dos partes visibles.
# 1 -  El relleno, que se aplica al área dentro del contorno de la forma:
shape.fill.fore_color = aspose.pydrawing.Color.white
# 2 -  El trazo, que marca el contorno de la forma:
# Modificar varias propiedades del trazo de esta forma.
stroke = shape.stroke
stroke.on = True
stroke.weight = 5
stroke.color = aspose.pydrawing.Color.red
stroke.dash_style = aw.drawing.DashStyle.SHORT_DASH_DOT_DOT
stroke.join_style = aw.drawing.JoinStyle.MITER
stroke.end_cap = aw.drawing.EndCap.SQUARE
stroke.line_style = aw.drawing.ShapeLineStyle.TRIPLE
stroke.fill.two_color_gradient(color1=aspose.pydrawing.Color.red, color2=aspose.pydrawing.Color.blue, style=aw.drawing.GradientStyle.VERTICAL, variant=aw.drawing.GradientVariant.VARIANT1)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Stroke.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Stroke](../)

