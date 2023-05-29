---
title: ShapeBase.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "ShapeBase.screen_tip property. Defines the text displayed when the mouse pointer moves over the shape."
type: docs
weight: 480
url: /python-net/aspose.words.drawing/shapebase/screen_tip/
---

## ShapeBase.screen_tip property

Defines the text displayed when the mouse pointer moves over the shape.

The default value is an empty string.




### Examples

Shows how to insert a shape which contains an image, and is also a hyperlink.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.href = "https://forum.aspose.com/"
shape.target = "New Window"
shape.screen_tip = "Aspose.Words Support Forums"

# Ctrl + left-clicking the shape in Microsoft Word will open a new web browser window
# and take us to the hyperlink in the "href" property.
doc.save(ARTIFACTS_DIR + "Image.insert_image_with_hyperlink.docx")
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

