---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /zh/python-net/aspose.words.drawing/shapebase/is_inline/
---

## ShapeBase.is_inline property

A quick way to determine if this shape is positioned inline with text.


```python
@property
def is_inline(self) -> bool:
    ...

```

### Remarks

Has effect only for top level shapes.




### Examples

Shows how to determine whether a shape is inline or floating.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 下面是形状可能具有的两种环绕类型。
# 1 -  行内：
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# 行内形状位于段落内部，和其他段落元素（如文本运行）一起。
# 在 Microsoft Word 中，我们可以像字符一样点击并拖动形状到任意段落。
# 如果形状很大，它会影响段落的垂直间距。
# 我们无法将此形状移动到没有段落的地方。
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  浮动：
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# 浮动形状属于我们插入的段落，
# 我们可以通过点击形状时出现的锚点符号来确定。
# 如果形状左侧没有可见的锚点符号，
# 我们需要通过 "Options" -> "Display" -> "Object Anchors" 来启用可见锚点。
# 在 Microsoft Word 中，我们可以左键单击并自由拖动此形状到任意位置。
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

