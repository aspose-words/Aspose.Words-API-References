﻿---
title: ShapeBase.behind_text property
linktitle: behind_text property
articleTitle: behind_text property
second_title: Aspose.Words for Python
description: "ShapeBase.behind_text property. Specifies whether the shape is below or above text."
type: docs
weight: 50
url: /python-net/aspose.words.drawing/shapebase/behind_text/
---

## ShapeBase.behind_text property

Specifies whether the shape is below or above text.


```python
@property
def behind_text(self) -> bool:
    ...

@behind_text.setter
def behind_text(self, value: bool):
    ...

```

### Remarks

Has effect only for top level shapes.

The default value is ``False``.




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

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)
* property [ShapeBase.z_order](../z_order/)

