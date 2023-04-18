---
title: wrap_type property
second_title: Aspose.Words for Python via .NET API Reference
description: "Defines whether the shape is inline or floating"
type: docs
weight: 600
url: /python-net/aspose.words.drawing/shapebase/wrap_type/
---

## ShapeBase.wrap_type property

Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.

The default value is [WrapType.NONE](../../wraptype/#NONE).

Has effect only for top level shapes.




### Examples

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER

doc.save(ARTIFACTS_DIR + "Image.create_floating_page_center.docx")
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
* class [ShapeBase](../)

