---
title: ShapeBase.bounds_in_points property
linktitle: bounds_in_points property
articleTitle: bounds_in_points property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds_in_points property. Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape."
type: docs
weight: 80
url: /es/python-net/aspose.words.drawing/shapebase/bounds_in_points/
---

## ShapeBase.bounds_in_points property

Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.


```python
@property
def bounds_in_points(self) -> aspose.pydrawing.RectangleF:
    ...

```

### Remarks

The returned bounds do not include the rotation of this shape or the rotation of the parent group shape, if any.


### Examples

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Aunque la línea en sí ocupa poco espacio en la página del documento,
# ocupa un bloque rectangular contenedor, cuyo tamaño podemos determinar usando las propiedades "Bounds".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Crea una forma de grupo y luego establece el tamaño de su bloque contenedor usando la propiedad "Bounds".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Crea un rectángulo, verifica el tamaño de su bloque delimitador y luego añádelo a la forma de grupo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# El plano de coordenadas de la forma de grupo tiene su origen en la esquina superior izquierda de su bloque contenedor,
# y las coordenadas x e y de (1000, 1000) en la esquina inferior derecha.
# Nuestra forma de grupo mide 250x250pt, por lo que cada 4pt en el plano de coordenadas de la forma de grupo
# se traduce a 1pt en el plano de coordenadas del cuerpo del documento.
# Cada forma que insertamos también se reducirá de tamaño en un factor de 4.
# El cambio en la propiedad "BoundsInPoints" de la forma reflejará esto.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Inserta una forma y colócala fuera de los límites del bloque contenedor de la forma de grupo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# La huella de la forma de grupo en el cuerpo del documento ha aumentado, pero el bloque contenedor sigue siendo el mismo.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

