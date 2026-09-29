---
title: ShapeBase.is_inline property
linktitle: is_inline property
articleTitle: is_inline property
second_title: Aspose.Words for Python
description: "ShapeBase.is_inline property. A quick way to determine if this shape is positioned inline with text."
type: docs
weight: 310
url: /ru/python-net/aspose.words.drawing/shapebase/is_inline/
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
# Ниже представлены два типа обтекания, которые могут иметь формы.
# 1 -  Встроенный:
builder.write('Hello world! ')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=100, height=100)
shape.fill_color = aspose.pydrawing.Color.light_blue
builder.write(' Hello again.')
# Встроенная фигура находится внутри абзаца среди других элементов абзаца, таких как фрагменты текста.
# В Microsoft Word мы можем щёлкнуть и перетащить фигуру в любой абзац, как если бы это был символ.
# Если фигура крупная, она будет влиять на вертикальное расстояние между абзацами.
# Мы не можем переместить эту фигуру в место без абзаца.
self.assertEqual(aw.drawing.WrapType.INLINE, shape.wrap_type)
self.assertTrue(shape.is_inline)
# 2 -  Плавающий:
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=200, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=200, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.fill_color = aspose.pydrawing.Color.orange
# Плавающая фигура принадлежит абзацу, в который мы её вставляем,
# что мы можем определить по символу якоря, появляющемуся при щелчке по фигуре.
# Если у фигуры слева нет видимого символа якоря,
# нам понадобится включить видимые якоря через "Options" -> "Display" -> "Object Anchors".
# В Microsoft Word мы можем левой кнопкой мыши свободно перетаскивать эту фигуру в любое место.
self.assertEqual(aw.drawing.WrapType.NONE, shape.wrap_type)
self.assertFalse(shape.is_inline)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.IsInline.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

