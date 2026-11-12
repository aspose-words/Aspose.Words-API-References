---
title: ShapeBase.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "ShapeBase.title property. Gets or sets the title (caption) of the current shape object."
type: docs
weight: 570
url: /ru/python-net/aspose.words.drawing/shapebase/title/
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
# Создайте форму, задайте ей заголовок и затем добавьте её в документ.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.width = 200
shape.height = 200
shape.title = 'My cube'
builder.insert_node(shape)
# Когда мы сохраняем документ с формой, у которой есть заголовок,
# Aspose.Words сохранит этот заголовок в альтернативном тексте формы.
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Title.docx')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'Shape.Title.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual('', shape.title)
self.assertEqual('Title: My cube', shape.alternative_text)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

