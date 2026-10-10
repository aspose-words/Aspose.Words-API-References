---
title: ShapeBase.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "ShapeBase.title property. Gets or sets the title (caption) of the current shape object."
type: docs
weight: 570
url: /zh/python-net/aspose.words.drawing/shapebase/title/
---

## ShapeBase.title property

Gets or sets the title (caption) of the current shape object.


```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Remarks

Default is empty string.

Cannot be ``None``, but can be an empty string.




### Examples

Shows how to set the title of a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个形状，给它一个标题，然后将其添加到文档中。
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.width = 200
shape.height = 200
shape.title = 'My cube'
builder.insert_node(shape)
# 当我们保存带有标题的形状的文档时，
# Aspose.Words 会将该标题存储在形状的 Alt Text 中。
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Title.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.Title.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual('', shape.title)
self.assertEqual('Title: My cube', shape.alternative_text)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

