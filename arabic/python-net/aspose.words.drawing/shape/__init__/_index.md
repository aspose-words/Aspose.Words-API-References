---
title: Shape constructor
linktitle: Shape constructor
articleTitle: Shape constructor
second_title: Aspose.Words for Python
description: "Shape constructor. Creates a new shape object."
type: docs
weight: 10
url: /ar/python-net/aspose.words.drawing/shape/__init__/
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
# المُنشئ العام لفئة "Shape" سيُنشئ شكلاً بنوع الترميز "ShapeMarkupLanguage.Vml".
# إذا كنت بحاجة لإنشاء شكل من نوع غير بدائي، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
# TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
# يرجى استخدام DocumentBuilder.InsertShape.
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
# إنشاء صندوق نص عائم.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# حدد المحاذاة الأفقية والعمودية للنص داخل الشكل.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# أضف فقرة إلى صندوق النص وأضف سلسلة نصية سيعرضها صندوق النص.
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

