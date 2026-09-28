---
title: Stroke.weight property
linktitle: weight property
articleTitle: weight property
second_title: Aspose.Words for Python
description: "Stroke.weight property. Defines the brush thickness that strokes the path of a shape in points."
type: docs
weight: 260
url: /zh/python-net/aspose.words.drawing/stroke/weight/
---

## Stroke.weight property

Defines the brush thickness that strokes the path of a shape in points.


```python
@property
def weight(self) -> float:
    ...

@weight.setter
def weight(self, value: float):
    ...

```

### Remarks

The default value for a [Shape](../../shape/) is 0.75.




### Examples

Shows how change stroke properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
# 基本形状，例如矩形，具有两个可见部分。
# 1 -  填充，适用于形状轮廓内部的区域：
shape.fill.fore_color = aspose.pydrawing.Color.white
# 2 -  描边，标记形状的轮廓：
# 修改此形状描边的各种属性。
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

