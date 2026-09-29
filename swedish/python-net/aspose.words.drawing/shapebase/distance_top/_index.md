---
title: ShapeBase.distance_top property
linktitle: distance_top property
articleTitle: distance_top property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_top property. Returns or sets the distance (in points) between the document text and the top edge of the shape."
type: docs
weight: 160
url: /sv/python-net/aspose.words.drawing/shapebase/distance_top/
---

## ShapeBase.distance_top property

Returns or sets the distance (in points) between the document text and the top edge of the shape.


```python
@property
def distance_top(self) -> float:
    ...

@distance_top.setter
def distance_top(self, value: float):
    ...

```

### Remarks

The default value is 0.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga en rektangel och låt texten omsluta dess gränser tätt.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Ställ in minsta avståndet mellan formen och omgivande text till 40pt från alla sidor.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Flytta formen närmare sidans centrum och rotera sedan formen 60 grader medurs.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Lägg till text som kommer att omsluta formen.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

