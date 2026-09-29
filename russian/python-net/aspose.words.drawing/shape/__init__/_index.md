---
title: Shape constructor
linktitle: Shape constructor
articleTitle: Shape constructor
second_title: Aspose.Words for Python
description: "Shape constructor. Creates a new shape object."
type: docs
weight: 10
url: /ru/python-net/aspose.words.drawing/shape/__init__/
---

## Shape(doc, shape_type) {#documentbase_shapetype}

Creates a new shape object.


```python
def __init__(self, doc: aspose.words.DocumentBase, shape_type: aspose.words.drawing.ShapeType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| shape_type | [ShapeType](../../shapetype/) | The type of the shape to create. |

### Remarks

You should specify desired shape properties after you created a shape.




### Examples

Shows how to insert a shape with an image from the local file system into a document.

```python
doc = aw.Document()
# Публичный конструктор класса "Shape" создаст фигуру с типом разметки "ShapeMarkupLanguage.Vml".
# Если вам нужно создать фигуру нестандартного типа, например SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded или DiagonalCornersRounded,
# пожалуйста, используйте DocumentBuilder.InsertShape.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
shape.image_data.set_image(file_name=IMAGE_DIR + 'Windows MetaFile.wmf')
shape.width = 100
shape.height = 100
doc.first_section.body.first_paragraph.append_child(shape)
doc.save(file_name=ARTIFACTS_DIR + 'Image.FromFile.docx')
```

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

