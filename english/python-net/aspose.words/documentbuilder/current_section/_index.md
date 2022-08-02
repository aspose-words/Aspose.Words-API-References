---
title: current_section property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets the section that is currently selected in this DocumentBuilder."
type: docs
weight: 60
url: /python-net/aspose.words/documentbuilder/current_section/
---

## DocumentBuilder.current_section property

Gets the section that is currently selected in this DocumentBuilder.


### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.wrap_type = aw.drawing.WrapType.NONE

# Configure the shape's "relative_horizontal_position" property to treat the value of the "left" property
# as the shape's horizontal distance, in points, from the left side of the page.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE

# Set the shape's horizontal distance from the left side of the page to 100.
shape.left = 100

# Use the "relative_vertical_position" property in a similar way to position the shape 80pt below the top of the page.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80

# Set the shape's height, which will automatically scale the width to preserve dimensions.
shape.height = 125

self.assertEqual(125.0, shape.width)

# The "bottom" and "right" properties contain the bottom and right edges of the image.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)

doc.save(ARTIFACTS_DIR + "Image.create_floating_position_size.docx")
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

