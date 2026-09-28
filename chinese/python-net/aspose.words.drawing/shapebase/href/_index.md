---
title: ShapeBase.href property
linktitle: href property
articleTitle: href property
second_title: Aspose.Words for Python
description: "ShapeBase.href property. Gets or sets the full hyperlink address for a shape."
type: docs
weight: 250
url: /zh/python-net/aspose.words.drawing/shapebase/href/
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
# 在 Microsoft Word 中按住 Ctrl 并左键单击该形状将打开一个新的网页浏览器窗口
# 并将我们带到 "HRef" 属性中的超链接。
doc.save(file_name=ARTIFACTS_DIR + 'Image.InsertImageWithHyperlink.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

