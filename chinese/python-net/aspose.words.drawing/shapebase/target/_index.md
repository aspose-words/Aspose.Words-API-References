---
title: ShapeBase.target property
linktitle: target property
articleTitle: target property
second_title: Aspose.Words for Python
description: "ShapeBase.target property. Gets or sets the target frame for the shape hyperlink."
type: docs
weight: 560
url: /zh/python-net/aspose.words.drawing/shapebase/target/
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
# 在 Microsoft Word 中按住 Ctrl 并左键单击该形状将打开一个新的网页浏览器窗口
# 并将我们带到 "HRef" 属性中的超链接。
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

