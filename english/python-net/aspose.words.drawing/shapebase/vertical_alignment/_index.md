﻿---
title: ShapeBase.vertical_alignment property
linktitle: vertical_alignment property
articleTitle: vertical_alignment property
second_title: Aspose.Words for Python
description: "ShapeBase.vertical_alignment property. Specifies how the shape is positioned vertically."
type: docs
weight: 600
url: /python-net/aspose.words.drawing/shapebase/vertical_alignment/
---

## ShapeBase.vertical_alignment property

Specifies how the shape is positioned vertically.


```python
@property
def vertical_alignment(self) -> aspose.words.drawing.VerticalAlignment:
    ...

@vertical_alignment.setter
def vertical_alignment(self, value: aspose.words.drawing.VerticalAlignment):
    ...

```

### Remarks

The default value is [VerticalAlignment.NONE](../../verticalalignment/#NONE).

Has effect only for top level floating shapes.




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

