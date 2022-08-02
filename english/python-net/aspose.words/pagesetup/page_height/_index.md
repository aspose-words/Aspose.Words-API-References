---
title: page_height property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns or sets the height of the page in points."
type: docs
weight: 300
url: /python-net/aspose.words/pagesetup/page_height/
---

## PageSetup.page_height property

Returns or sets the height of the page in points.


### Examples

Shows how to insert an image, and use it as a watermark.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert the image into the header so that it will be visible on every page.
image = drawing.Image.from_file(IMAGE_DIR + "Transparent background logo.png")
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
shape = builder.insert_image(image)
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True

# Place the image at the center of the page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.left = (builder.page_setup.page_width - shape.width) // 2
shape.top = (builder.page_setup.page_height - shape.height) // 2

doc.save(ARTIFACTS_DIR + "DocumentBuilder.insert_watermark.docx")
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

