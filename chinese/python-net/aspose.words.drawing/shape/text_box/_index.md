---
title: Shape.text_box property
linktitle: text_box property
articleTitle: text_box property
second_title: Aspose.Words for Python
description: "Shape.text_box property. Defines attributes that specify how text is displayed in a shape."
type: docs
weight: 230
url: /zh/python-net/aspose.words.drawing/shape/text_box/
---

## Shape.text_box property

Defines attributes that specify how text is displayed in a shape.


```python
@property
def text_box(self) -> aspose.words.drawing.TextBox:
    ...

```

### Examples

Shows how to set the orientation of text inside a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# 将文档生成器移动到 TextBox 内部并添加文本。
builder.move_to(text_box_shape.last_paragraph)
builder.writeln('Hello world!')
builder.write('Hello again!')
# 将 "LayoutFlow" 属性设置为此文本框中文本内容的方向。
text_box.layout_flow = layout_flow
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxLayoutFlow.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

