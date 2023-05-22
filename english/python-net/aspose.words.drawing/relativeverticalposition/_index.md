---
title: RelativeVerticalPosition enumeration
linktitle: RelativeVerticalPosition enumeration
articleTitle: RelativeVerticalPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.RelativeVerticalPosition enumeration. Specifies to what the vertical position of a shape or text frame is relative."
type: docs
weight: 280
url: /python-net/aspose.words.drawing/relativeverticalposition/
---

## RelativeVerticalPosition enumeration

Specifies to what the vertical position of a shape or text frame is relative.


### Members

| Name | Description |
| --- | --- |
| MARGIN | Specifies that the vertical positioning shall be relative to the page margins. |
| PAGE | The object is positioned relative to the top edge of the page. |
| PARAGRAPH | The object is positioned relative to the top of the paragraph that contains the anchor. |
| LINE | Undocumented. |
| TOP_MARGIN | Specifies that the vertical positioning shall be relative to the top margin of the current page. |
| BOTTOM_MARGIN | Specifies that the vertical positioning shall be relative to the bottom margin of the current page. |
| INSIDE_MARGIN | Specifies that the vertical positioning shall be relative to the inside margin of the current page. |
| OUTSIDE_MARGIN | Specifies that the vertical positioning shall be relative to the outside margin of the current page. |
| TABLE_DEFAULT | Default value is [RelativeVerticalPosition.MARGIN](./#MARGIN). |
| TEXT_FRAME_DEFAULT | Default value is [RelativeVerticalPosition.PARAGRAPH](./#PARAGRAPH). |

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

* module [aspose.words.drawing](../)
* property [ShapeBase.relative_vertical_position](../shapebase/relative_vertical_position/)

