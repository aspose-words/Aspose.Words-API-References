---
title: ShapeBase.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "ShapeBase.screen_tip property. Defines the text displayed when the mouse pointer moves over the shape."
type: docs
weight: 510
url: /it/python-net/aspose.words.drawing/shapebase/screen_tip/
---

## ShapeBase.screen_tip property

Defines the text displayed when the mouse pointer moves over the shape.


```python
@property
def screen_tip(self) -> str:
    ...

@screen_tip.setter
def screen_tip(self, value: str):
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
# Ctrl + clic sinistro sulla forma in Microsoft Word aprirà una nuova finestra del browser web.
# e portaci al collegamento ipertestuale nella proprietà "HRef".
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

