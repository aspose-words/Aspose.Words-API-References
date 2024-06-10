---
title: ShapeBase.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "ShapeBase.name property. Gets or sets the optional shape name."
type: docs
weight: 410
url: /python-net/aspose.words.drawing/shapebase/name/
---

## ShapeBase.name property

Gets or sets the optional shape name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Remarks

Default is empty string.

Cannot be ``None``, but can be an empty string.




### Examples

Shows how to use a shape's alternative text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
shape = builder.insert_shape(aw.drawing.ShapeType.CUBE, 150, 150)
shape.name = 'MyCube'
shape.alternative_text = 'Alt text for MyCube.'
# We can access the alternative text of a shape by right-clicking it, and then via "Format AutoShape" -> "Alt Text".
doc.save(ARTIFACTS_DIR + 'Shape.alt_text.docx')
# Save the document to HTML, and then delete the linked image that belongs to our shape.
# The browser that is reading our HTML will display the alt text in place of the missing image.
doc.save(ARTIFACTS_DIR + 'Shape.alt_text.html')
os.remove(ARTIFACTS_DIR + 'Shape.alt_text.001.png')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

