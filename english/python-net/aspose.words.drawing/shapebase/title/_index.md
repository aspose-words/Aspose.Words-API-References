---
title: ShapeBase.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "ShapeBase.title property. Gets or sets the title (caption) of the current shape object."
type: docs
weight: 570
url: /python-net/aspose.words.drawing/shapebase/title/
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
builder = aw.DocumentBuilder(doc)
# Create a shape, give it a title, and then add it to the document.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
shape.width = 200
shape.height = 200
shape.title = 'My cube'
builder.insert_node(shape)
# When we save a document with a shape that has a title,
# Aspose.Words will store that title in the shape's Alt Text.
doc.save(ARTIFACTS_DIR + 'Shape.title.docx')
doc = aw.Document(ARTIFACTS_DIR + 'Shape.title.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
self.assertEqual('', shape.title)
self.assertEqual('Title: My cube', shape.alternative_text)
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

