---
title: ShapeBase.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "ShapeBase.screen_tip property. Defines the text displayed when the mouse pointer moves over the shape."
type: docs
weight: 510
url: /tr/python-net/aspose.words.drawing/shapebase/screen_tip/
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
# Microsoft Word'de şekle Ctrl + sol tıklama yapmak yeni bir web tarayıcısı penceresi açar
# ve bizi "HRef" özelliğindeki bağlantıya götürün.
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

