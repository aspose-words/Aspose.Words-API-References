---
title: Stroke.line_style property
linktitle: line_style property
articleTitle: line_style property
second_title: Aspose.Words for Python
description: "Stroke.line_style property. Defines the line style of the stroke."
type: docs
weight: 180
url: /fr/python-net/aspose.words.drawing/stroke/line_style/
---

## Stroke.line_style property

Defines the line style of the stroke.


```python
@property
def line_style(self) -> aspose.words.drawing.ShapeLineStyle:
    ...

@line_style.setter
def line_style(self, value: aspose.words.drawing.ShapeLineStyle):
    ...

```

### Remarks

The default value is [ShapeLineStyle.SINGLE](../../shapelinestyle/#SINGLE).




### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
# Les formes de base, comme le rectangle, ont deux parties visibles.
# 1 -  Le remplissage, qui s'applique à la zone à l'intérieur du contour de la forme :
shape.fill.fore_color = aspose.pydrawing.Color.white
# 2 -  Le trait, qui délimite le contour de la forme :
# Modifier diverses propriétés du trait de cette forme.
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

