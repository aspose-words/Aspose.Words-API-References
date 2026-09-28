---
title: ShapeBase.screen_tip property
linktitle: screen_tip property
articleTitle: screen_tip property
second_title: Aspose.Words for Python
description: "ShapeBase.screen_tip property. Defines the text displayed when the mouse pointer moves over the shape."
type: docs
weight: 510
url: /zh/python-net/aspose.words.drawing/shapebase/screen_tip/
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
# 在 Microsoft Word 中按住 Ctrl 并左键单击该形状将打开一个新的网页浏览器窗口
# 并将我们带到 "HRef" 属性中的超链接。
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

