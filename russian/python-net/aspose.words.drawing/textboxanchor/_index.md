---
title: TextBoxAnchor enumeration
linktitle: TextBoxAnchor enumeration
articleTitle: TextBoxAnchor enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextBoxAnchor enumeration. Specifies values used for shape text vertical alignment."
type: docs
weight: 460
url: /ru/python-net/aspose.words.drawing/textboxanchor/
---

## TextBoxAnchor enumeration

Specifies values used for shape text vertical alignment.


### Members

| Name | Description |
| --- | --- |
| TOP | Text is aligned to the top of the textbox. |
| MIDDLE | Text is aligned to the middle of the textbox. |
| BOTTOM | Text is aligned to the bottom of the textbox. |
| TOP_CENTERED | Text is aligned to the top centered of the textbox. |
| MIDDLE_CENTERED | Text is aligned to the middle centered of the textbox. |
| BOTTOM_CENTERED | Text is aligned to the bottom centered of the textbox. |
| TOP_BASELINE | Text is aligned to the top baseline of the textbox. |
| BOTTOM_BASELINE | Text is aligned to the bottom baseline of the textbox. |
| TOP_CENTERED_BASELINE | Text is aligned to the top centered baseline of the textbox. |
| BOTTOM_CENTERED_BASELINE | Text is aligned to the bottom centered baseline of the textbox. |

### Examples

Shows how to vertically align the text contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=200, height=200)
# Установите свойство "VerticalAnchor" в "TextBoxAnchor.Top", чтобы
# выравнивать текст в этом текстовом поле по верхней стороне фигуры.
# Установите свойство "VerticalAnchor" в "TextBoxAnchor.Middle", чтобы
# выравнивать текст в этом текстовом поле по центру фигуры.
# Установите свойство "VerticalAnchor" в "TextBoxAnchor.Bottom", чтобы
# выравнивать текст в этом текстовом поле к нижней части фигуры.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# Вертикальное выравнивание текста внутри текстовых полей доступно, начиная с Microsoft Word 2007.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.VerticalAnchor.docx')
```

### See Also

* module [aspose.words.drawing](../)

