---
title: VerticalAlignment enumeration
linktitle: VerticalAlignment enumeration
articleTitle: VerticalAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.VerticalAlignment enumeration. Specifies vertical alignment of a floating shape, text frame or a floating table."
type: docs
weight: 510
url: /python-net/aspose.words.drawing/verticalalignment/
---

## VerticalAlignment enumeration

Specifies vertical alignment of a floating shape, text frame or a floating table.


### Members

| Name | Description |
| --- | --- |
| NONE | The object is explicitly positioned, usually using its **Top** property. |
| TOP | Specifies that the object shall be at the top of the vertical alignment base. |
| CENTER | Specifies that the object shall be centered with respect to the vertical alignment base. |
| BOTTOM | Specifies that the object shall be at the bottom of the vertical alignment base. |
| INSIDE | Specifies that the object shall be inside of the horizontal alignment base. |
| OUTSIDE | Specifies that the object shall be outside of the vertical alignment base. |
| INLINE | Not documented. Seems to be a possible value for floating paragraphs and tables. |
| DEFAULT | Same as [VerticalAlignment.NONE](./#NONE). |

### Examples

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
* property [ShapeBase.vertical_alignment](../shapebase/vertical_alignment/)

