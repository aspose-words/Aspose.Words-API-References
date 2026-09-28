---
title: ShapeBase.z_order property
linktitle: z_order property
articleTitle: z_order property
second_title: Aspose.Words for Python
description: "ShapeBase.z_order property. Determines the display order of overlapping shapes."
type: docs
weight: 650
url: /zh/python-net/aspose.words.drawing/shapebase/z_order/
---

## ShapeBase.z_order property

Determines the display order of overlapping shapes.


```python
@property
def z_order(self) -> int:
    ...

@z_order.setter
def z_order(self, value: int):
    ...

```

### Remarks

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed
as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main
text of the document.

The display order of child shapes in a group shape is determined by their order
inside the group shape.




### Examples

Shows how to manipulate the order of shapes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入三个不同颜色的矩形，使它们部分重叠。
# 当我们插入一个与另一个形状重叠的形状时，Aspose.Words 会将较新的形状放在旧的形状之上。
# 浅绿色矩形将覆盖浅蓝色矩形并部分遮挡它，
# 而浅蓝色矩形将遮挡橙色矩形。
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=100, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=150, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=150, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_blue
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=200, height=200, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.light_green
shapes = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_shape(), b), list(doc.get_child_nodes(aw.NodeType.SHAPE, True)))))
# 形状的 "ZOrder" 属性决定其在其他重叠形状中的堆叠优先级。
# 如果两个重叠形状的 "ZOrder" 值不同，
# Microsoft Word 会将值较高的形状放在值较低的形状之上。
# 设置我们形状的 "ZOrder" 值，使第一个橙色矩形位于第二个浅蓝色矩形之上
# 并使第二个浅蓝色矩形位于第三个浅绿色矩形之上。
# 这将颠倒它们原来的堆叠顺序。
shapes[0].z_order = 3
shapes[1].z_order = 2
shapes[2].z_order = 1
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ZOrder.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)
* property [ShapeBase.behind_text](../behind_text/)

