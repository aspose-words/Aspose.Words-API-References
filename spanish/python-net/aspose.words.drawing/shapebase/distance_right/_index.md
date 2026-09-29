---
title: ShapeBase.distance_right property
linktitle: distance_right property
articleTitle: distance_right property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_right property. Returns or sets the distance (in points) between the document text and the right edge of the shape."
type: docs
weight: 150
url: /es/python-net/aspose.words.drawing/shapebase/distance_right/
---

## ShapeBase.distance_right property

Returns or sets the distance (in points) between the document text and the right edge of the shape.


```python
@property
def distance_right(self) -> float:
    ...

@distance_right.setter
def distance_right(self, value: float):
    ...

```

### Remarks

The default value is 1/8 inch.

Has effect only for top level shapes.




### Examples

Shows how to set the wrapping distance for a text that surrounds a shape.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserta un rectángulo y haz que el texto se ajuste estrechamente a sus límites.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Establece la distancia mínima entre la forma y el texto circundante a 40pt en todos los lados.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Mueve la forma más cerca del centro de la página y luego rota la forma 60 grados en sentido horario.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Añade texto que se ajuste alrededor de la forma.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

