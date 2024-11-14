---
title: HorizontalAlignment enumeration
linktitle: HorizontalAlignment enumeration
articleTitle: HorizontalAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.HorizontalAlignment enumeration. Specifies horizontal alignment of a floating shape, text frame or floating table."
type: docs
weight: 170
url: /python-net/aspose.words.drawing/horizontalalignment/
---

## HorizontalAlignment enumeration

Specifies horizontal alignment of a floating shape, text frame or floating table.


### Members

| Name | Description |
| --- | --- |
| NONE | The object is explicitly positioned, usually using its **Left** property. |
| DEFAULT | Same as [HorizontalAlignment.NONE](./#NONE). |
| LEFT | Specifies that the object shall be left aligned to the horizontal alignment base. |
| CENTER | Specifies that the object shall be centered with respect to the horizontal alignment base. |
| RIGHT | Specifies that the object shall be right aligned to the horizontal alignment base. |
| INSIDE | Specifies that the object shall be inside of the horizontal alignment base. |
| OUTSIDE | Specifies that the object shall be outside of the horizontal alignment base. |

### Examples

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPageCenter.docx')
```

### See Also

* module [aspose.words.drawing](../)
* property [ShapeBase.horizontal_alignment](../shapebase/horizontal_alignment/)

