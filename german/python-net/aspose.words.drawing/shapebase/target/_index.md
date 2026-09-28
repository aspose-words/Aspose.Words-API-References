---
title: ShapeBase.target property
linktitle: target property
articleTitle: target property
second_title: Aspose.Words for Python
description: "ShapeBase.target property. Gets or sets the target frame for the shape hyperlink."
type: docs
weight: 560
url: /de/python-net/aspose.words.drawing/shapebase/target/
---

## ShapeBase.target property

Gets or sets the target frame for the shape hyperlink.


```python
@property
def target(self) -> str:
    ...

@target.setter
def target(self, value: str):
    ...

```

### Remarks

The default value is an empty string.




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

