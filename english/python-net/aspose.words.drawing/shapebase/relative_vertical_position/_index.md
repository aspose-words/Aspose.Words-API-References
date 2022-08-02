---
title: relative_vertical_position property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies relative to what the shape is positioned vertically."
type: docs
weight: 410
url: /python-net/aspose.words.drawing/shapebase/relative_vertical_position/
---

## ShapeBase.relative_vertical_position property

Specifies relative to what the shape is positioned vertically.

The default value is [RelativeVerticalPosition.PARAGRAPH](../../relativeverticalposition/#PARAGRAPH).

Has effect only for top level floating shapes.




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

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

