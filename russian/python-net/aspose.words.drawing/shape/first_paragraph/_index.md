---
title: Shape.first_paragraph property
linktitle: first_paragraph property
articleTitle: first_paragraph property
second_title: Aspose.Words for Python
description: "Shape.first_paragraph property. Gets the first paragraph in the shape."
type: docs
weight: 70
url: /ru/python-net/aspose.words.drawing/shape/first_paragraph/
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
# Создайте плавающий текстовый блок.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# Установите горизонтальное и вертикальное выравнивание текста внутри фигуры.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# Добавьте абзац в текстовый блок и добавьте фрагмент текста, который будет отображаться в текстовом блоке.
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

