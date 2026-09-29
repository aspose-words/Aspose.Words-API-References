---
title: Shape constructor
linktitle: Shape constructor
articleTitle: Shape constructor
second_title: Aspose.Words for Python
description: "Shape constructor. Creates a new shape object."
type: docs
weight: 10
url: /tr/python-net/aspose.words.drawing/shape/__init__/
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
# "Shape" sınıfının genel yapıcı metodu, "ShapeMarkupLanguage.Vml" işaretleme türüne sahip bir şekil oluşturur.
# SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi ilkel olmayan bir türde şekil oluşturmanız gerekiyorsa,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
# lütfen DocumentBuilder.InsertShape metodunu kullanın.
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
# Yüzen bir metin kutusu oluşturun.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200
# Şeklin içindeki metnin yatay ve dikey hizalamasını ayarlayın.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP
# Metin kutusuna bir paragraf ekleyin ve metin kutusunun göstereceği bir metin çalışması ekleyin.
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

