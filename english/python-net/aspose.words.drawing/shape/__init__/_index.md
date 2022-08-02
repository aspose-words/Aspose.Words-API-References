---
title: Shape constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "Creates a new shape object."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/shape/__init__/
---

## Shape(doc, shape_type) {#documentbase_shapetype}

Creates a new shape object.


```python
def __init__(self, doc: aspose.words.DocumentBase, shape_type: aspose.words.drawing.ShapeType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) |  |
| shape_type | [ShapeType](../../shapetype/) |  |

You should specify desired shape properties after you created a shape.




### Examples

Shows how to insert a shape with an image from the local file system into a document.

```python
doc = aw.Document()

# The "Shape" class's public constructor will create a shape with "ShapeMarkupLanguage.VML" markup type.
# If you need to create a shape of a non-primitive type, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, or DiagonalCornersRounded,
# please use DocumentBuilder.insert_shape.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
shape.image_data.set_image(IMAGE_DIR + "Windows MetaFile.wmf")
shape.width = 100
shape.height = 100

doc.first_section.body.first_paragraph.append_child(shape)

doc.save(ARTIFACTS_DIR + "Image.from_file.docx")
```

Shows how to create and format a text box.

```python
doc = aw.Document()

# Create a floating text box.
text_box = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
text_box.wrap_type = aw.drawing.WrapType.NONE
text_box.height = 50
text_box.width = 200

# Set the horizontal, and vertical alignment of the text inside the shape.
text_box.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
text_box.vertical_alignment = aw.drawing.VerticalAlignment.TOP

# Add a paragraph to the text box and add a run of text that the text box will display.
text_box.append_child(aw.Paragraph(doc))
para = text_box.first_paragraph
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
run = aw.Run(doc)
run.text = "Hello world!"
para.append_child(run)

doc.first_section.body.first_paragraph.append_child(text_box)

doc.save(ARTIFACTS_DIR + "Shape.create_text_box.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

