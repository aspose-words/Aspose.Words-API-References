---
title: ShapeBase.href property
linktitle: href property
articleTitle: href property
second_title: Aspose.Words for Python
description: "ShapeBase.href property. Gets or sets the full hyperlink address for a shape."
type: docs
weight: 250
url: /de/python-net/aspose.words.drawing/shapebase/href/
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
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.href = 'https://forum.aspose.com/'
shape.target = 'New Window'
shape.screen_tip = 'Aspose.Words Support Forums'
# Strg + Linksklick auf die Form in Microsoft Word öffnet ein neues Browserfenster
# und führen Sie uns zum Hyperlink in der "HRef"-Eigenschaft.
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

