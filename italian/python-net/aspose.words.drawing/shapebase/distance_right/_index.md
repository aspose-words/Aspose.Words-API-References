---
title: ShapeBase.distance_right property
linktitle: distance_right property
articleTitle: distance_right property
second_title: Aspose.Words for Python
description: "ShapeBase.distance_right property. Returns or sets the distance (in points) between the document text and the right edge of the shape."
type: docs
weight: 150
url: /it/python-net/aspose.words.drawing/shapebase/distance_right/
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
# Inserisci un rettangolo e, fai avvolgere il testo strettamente attorno ai suoi limiti.
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.RECTANGLE, width=150, height=150)
shape.wrap_type = aw.drawing.WrapType.TIGHT
# Imposta la distanza minima tra la forma e il testo circostante a 40pt su tutti i lati.
shape.distance_top = 40
shape.distance_bottom = 40
shape.distance_left = 40
shape.distance_right = 40
# Sposta la forma più vicino al centro della pagina, quindi ruota la forma di 60 gradi in senso orario.
shape.top = 75
shape.left = 150
shape.rotation = 60
# Aggiungi del testo che avvolga la forma.
builder.font.size = 24
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + 'Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Coordinates.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

