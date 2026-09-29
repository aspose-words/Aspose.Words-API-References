---
title: ShapeBase.height property
linktitle: height property
articleTitle: height property
second_title: Aspose.Words for Python
description: "ShapeBase.height property. Gets or sets the height of the containing block of the shape."
type: docs
weight: 210
url: /es/python-net/aspose.words.drawing/shapebase/height/
---

## ShapeBase.height property

Gets or sets the height of the containing block of the shape.


```python
@property
def height(self) -> float:
    ...

@height.setter
def height(self, value: float):
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

Shows how to resize a shape with an image.

```python
# Cuando insertamos una imagen usando el método "InsertImage", el generador escala la forma que muestra la imagen de modo que,
# cuando vemos el documento con un zoom del 100 % en Microsoft Word, la forma muestra la imagen en su tamaño real.
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Una imagen de 400 x 400 creará un objeto ImageData con un tamaño de imagen de 300 x 300 pt.
image_size = shape.image_data.image_size
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Si las dimensiones de una forma coinciden con las dimensiones de los datos de la imagen,
# entonces la forma muestra la imagen en su tamaño original.
self.assertEqual(300, shape.width)
self.assertEqual(300, shape.height)
# Reduzca el tamaño total de la forma en un 50 %.
# Los factores de escala se aplican tanto al ancho como a la altura simultáneamente para preservar las proporciones de la forma.
shape.width *= 0.5
self.assertEqual(150, shape.width)
self.assertEqual(150, shape.height)
# Al redimensionar la forma, el tamaño de los datos de la imagen permanece igual.
self.assertEqual(300, image_size.width_points)
self.assertEqual(300, image_size.height_points)
# Podemos referirnos a las dimensiones de los datos de la imagen para aplicar una escala basada en el tamaño de la imagen.
shape.width = image_size.width_points * 1.1
self.assertEqual(330, shape.width)
self.assertEqual(330, shape.height)
doc.save(file_name=ARTIFACTS_DIR + 'Image.ScaleImage.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

