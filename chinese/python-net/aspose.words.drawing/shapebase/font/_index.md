---
title: ShapeBase.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "ShapeBase.font property. Provides access to the font formatting of this object."
type: docs
weight: 190
url: /zh/python-net/aspose.words.drawing/shapebase/font/
---

## ShapeBase.font property

Provides access to the font formatting of this object.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Examples

Shows how to insert a text box, and set the font of its contents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=300, height=50)
builder.move_to(shape.last_paragraph)
builder.write('This text is inside the text box.')
# 将形状的 "Font" 对象的 "Hidden" 属性设为 "true" 以隐藏文本框
# 并折叠其通常占用的空间。
# 将形状的 "Font" 对象的 "Hidden" 属性设为 "false" 以保持文本框可见。
shape.font.hidden = hide_shape
# 如果形状可见，我们将通过字体对象修改其外观。
if not hide_shape:
    shape.font.highlight_color = aspose.pydrawing.Color.light_gray
    shape.font.color = aspose.pydrawing.Color.red
    shape.font.underline = aw.Underline.DASH
# 将构建器从文本框移回主文档。
builder.move_to(shape.parent_paragraph)
builder.writeln('\nThis text is outside the text box.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Font.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

