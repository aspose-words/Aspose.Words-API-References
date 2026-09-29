---
title: ShapeBase.width property
linktitle: width property
articleTitle: width property
second_title: Aspose.Words for Python
description: "ShapeBase.width property. Gets or sets the width of the containing block of the shape."
type: docs
weight: 610
url: /it/python-net/aspose.words.drawing/shapebase/width/
---

## ShapeBase.width property

Gets or sets the width of the containing block of the shape.


```python
@property
def width(self) -> float:
    ...

@width.setter
def width(self, value: float):
    ...

```

### Remarks

For a top-level shape, the value is in points.

For shapes in a group, the value is in the coordinate space and units of the parent group.

The default value is 0.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Configura la proprietà "RelativeHorizontalPosition" della forma in modo che tratti il valore della proprietà "Left"
# come la distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Imposta la distanza orizzontale della forma dal lato sinistro della pagina a 100.
shape.left = 100
# Usa la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Imposta l'altezza della forma, che scalerà automaticamente la larghezza per preservare le dimensioni.
shape.height = 125
self.assertEqual(125, shape.width)
# Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

Shows how to resize a shape with an image.

```python
# Quando inseriamo un'immagine usando il metodo "InsertImage", il builder scala la forma che visualizza l'immagine in modo che,
# quando visualizziamo il documento con zoom al 100% in Microsoft Word, la forma visualizza l'immagine nella sua dimensione reale.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Un'immagine 400x400 creerà un oggetto ImageData con una dimensione dell'immagine di 300x300pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Se le dimensioni di una forma corrispondono alle dimensioni dei dati dell'immagine,
# allora la forma visualizza l'immagine nella sua dimensione originale.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Riduci la dimensione complessiva della forma del 50%.
# I fattori di scala si applicano sia alla larghezza che all'altezza contemporaneamente per preservare le proporzioni della forma.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Quando ridimensioni la forma, la dimensione dei dati dell'immagine rimane invariata.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Possiamo fare riferimento alle dimensioni dei dati dell'immagine per applicare una scala basata sulla dimensione dell'immagine.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

