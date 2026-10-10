---
title: Shape.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "Shape.first_paragraph property. Gets the first paragraph in the shape."
type: docs
weight: 70
url: /zh/python-net/aspose.words.drawing/shape/first_paragraph/
---

## Shape.first_paragraph property

Gets the first paragraph in the shape.


```python
@property
def first_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to create and format a text box.

```python
doc = aw.Document()
# 创建一个浮动文本框。
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# 设置形状内部文本的水平和垂直对齐方式。
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# 向文本框添加一个段落，并添加一段文本运行，文本框将显示该文本。
text_box.append_child(aw.Paragraph(doc))
para = text_box.first_paragraph
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
run = aw.Run(doc=doc)
run.text = 'Hello world!'
para.append_child(run)
doc.first_section.body.first_paragraph.append_child(text_box)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.CreateTextBox.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

