---
title: ShapeBase.bottom property
linktitle: bottom property
articleTitle: bottom property
second_title: Aspose.Words for Python
description: "ShapeBase.bottom property. Gets the position of the bottom edge of the containing block of the shape."
type: docs
weight: 60
url: /es/python-net/aspose.words.drawing/shapebase/bottom/
---

## ShapeBase.bottom property

Gets the position of the bottom edge of the containing block of the shape.


```python
@property
def bottom(self) -> float:
    ...

```

### Remarks

For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to insert a floating image, and specify its position and size.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
shape.wrap_type = aw.drawing.WrapType.NONE
# Configure la propiedad "RelativeHorizontalPosition" de la forma para que trate el valor de la propiedad "Left"
# como la distancia horizontal de la forma, en puntos, desde el lado izquierdo de la página.
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
# Establezca la distancia horizontal de la forma desde el lado izquierdo de la página a 100.
shape.left = 100
# Utilice la propiedad "RelativeVerticalPosition" de manera similar para posicionar la forma 80 pt por debajo de la parte superior de la página.
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.top = 80
# Establezca la altura de la forma, lo que escalará automáticamente el ancho para preservar las dimensiones.
shape.height = 125
self.assertEqual(125, shape.width)
# Las propiedades "Bottom" y "Right" contienen los bordes inferior y derecho de la imagen.
self.assertEqual(shape.top + shape.height, shape.bottom)
self.assertEqual(shape.left + shape.width, shape.right)
doc.save(file_name=ARTIFACTS_DIR + 'Image.CreateFloatingPositionSize.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

