---
title: ShapeBase.alternative_text property
linktitle: alternative_text property
articleTitle: alternative_text property
second_title: Aspose.Words for Python
description: "ShapeBase.alternative_text property. Defines alternative text to be displayed instead of a graphic."
type: docs
weight: 20
url: /sv/python-net/aspose.words.drawing/shapebase/alternative_text/
---

## ShapeBase.alternative_text property

Defines alternative text to be displayed instead of a graphic.


```python
@property
def alternative_text(self) -> str:
    ...

@alternative_text.setter
def alternative_text(self, value: str):
    ...

```

### Remarks

The default value is an empty string.




### Examples

Shows how to use a shape's alternative text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.CUBE, width=150, height=150)
shape.name = 'MyCube'
shape.alternative_text = 'Alt text for MyCube.'
# Vi kan komma åt alternativ text för en form genom att högerklicka på den, och sedan via "Format AutoShape" -> "Alt Text".
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.docx')
# Spara dokumentet som HTML, och ta sedan bort den länkade bilden som tillhör vår form.
# Webbläsaren som läser vår HTML kommer att visa alt-texten i stället för den saknade bilden.
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AltText.html')
os.unlink(ARTIFACTS_DIR + 'Shape.AltText.001.png')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

