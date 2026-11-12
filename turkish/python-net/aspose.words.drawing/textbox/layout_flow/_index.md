---
title: TextBox.layout_flow property
linktitle: layout_flow property
articleTitle: layout_flow property
second_title: Aspose.Words for Python
description: "TextBox.layout_flow property. Determines the flow of the text layout in a shape."
type: docs
weight: 60
url: /tr/python-net/aspose.words.drawing/textbox/layout_flow/
---

## TextBox.layout_flow property

Determines the flow of the text layout in a shape.


```python
@property
def layout_flow(self) -> aspose.words.drawing.LayoutFlow:
    ...

@layout_flow.setter
def layout_flow(self, value: aspose.words.drawing.LayoutFlow):
    ...

```

### Remarks

The default value is [LayoutFlow.HORIZONTAL](../../layoutflow/#HORIZONTAL).




### Examples

Shows how to set the orientation of text inside a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
text_box_shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=150, height=100)
text_box = text_box_shape.text_box
# Belge oluşturucuyu TextBox içine taşıyın ve metin ekleyin.
builder.move_to(text_box_shape.last_paragraph)
builder.writeln('Hello world!')
builder.write('Hello again!')
# "LayoutFlow" özelliğini bu metin kutusunun metin içeriği için bir yön ayarlamak üzere ayarlayın.
text_box.layout_flow = layout_flow
doc.save(file_name=ARTIFACTS_DIR + 'Shape.TextBoxLayoutFlow.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

