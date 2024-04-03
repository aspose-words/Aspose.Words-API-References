---
title: ShapeBase.href property
linktitle: href property
articleTitle: href property
second_title: Aspose.Words for Python
description: "ShapeBase.href property. Gets or sets the full hyperlink address for a shape."
type: docs
weight: 240
url: /python-net/aspose.words.drawing/shapebase/href/
---

## ShapeBase.href property

Gets or sets the full hyperlink address for a shape.


```python
@property
def href(self) -> str:
    ...

@href.setter
def href(self, value: str):
    ...

```

### Remarks

The default value is an empty string.

Below are examples of valid values for this property:

Full URI: ``https://www.aspose.com/``.

Full file name: ``C:\\\\My Documents\\\\SalesReport.doc``.

Relative URI: ``../../../resource.txt``


Relative file name: ``..\\\\My Documents\\\\SalesReport.doc``.

Bookmark within another document: ``https://www.aspose.com/Products/Default.aspx#Suites``


Bookmark within this document: ``#BookmakName``.




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

