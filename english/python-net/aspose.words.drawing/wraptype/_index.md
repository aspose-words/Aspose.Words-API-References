---
title: WrapType enumeration
linktitle: WrapType enumeration
articleTitle: WrapType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.WrapType enumeration. Specifies how text is wrapped around a shape or picture."
type: docs
weight: 530
url: /python-net/aspose.words.drawing/wraptype/
---

## WrapType enumeration

Specifies how text is wrapped around a shape or picture.


### Members

| Name | Description |
| --- | --- |
| NONE | No text wrapping around the shape. The shape is placed behind or in front of text. |
| INLINE | The shape remains on the same layer as text and treated as a character. |
| TOP_BOTTOM | The text stops at the top of the shape and restarts on the line below the shape. |
| SQUARE | Wraps text around all sides of the square bounding box of the shape. |
| TIGHT | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| THROUGH | Same as Tight, but wraps inside any parts of the shape that are open. |

### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert the image into the header so that it will be visible on every page.
image = aspose.pydrawing.Image.from_file(IMAGE_DIR + 'Transparent background logo.png')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(image)
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
# Place the image at the center of the page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) // 2
shape.top = (builder.page_setup.page_height - shape.height) // 2
doc.save(ARTIFACTS_DIR + 'DocumentBuilder.insert_watermark.docx')
```

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
shape = builder.insert_image(IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER
doc.save(ARTIFACTS_DIR + 'Image.create_floating_page_center.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.wrap_type](../shapebase/wrap_type/)

