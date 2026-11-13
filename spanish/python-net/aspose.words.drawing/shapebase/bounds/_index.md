---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /es/python-net/aspose.words.drawing/shapebase/bounds/
---

## ShapeBase.bounds property

Gets or sets the location and size of the containing block of the shape.


```python
@property
def bounds(self) -> aspose.pydrawing.RectangleF:
    ...

@bounds.setter
def bounds(self, value: aspose.pydrawing.RectangleF):
    ...

```

### Remarks

Ignores aspect ratio lock upon setting.


For a top-level shape, the value is in points and relative to the shape anchor.

For shapes in a group, the value is in the coordinate space and units of the parent group.




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# Cree un grupo de formas. Un grupo de formas puede mostrar una colección de nodos de formas hijas.
# En Microsoft Word, hacer clic dentro del límite del grupo de formas o en una de las formas hijas del grupo de formas
# seleccionará todas las demás formas hijas dentro de este grupo y nos permitirá escalar y mover todas las formas a la vez.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Cree un grupo de formas de 400pt x 400pt y colóquelo en el origen de coordenadas de formas flotantes del documento.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Establezca el tamaño del plano de coordenadas interno del grupo en 500 x 500pt.
# La esquina superior izquierda del grupo tendrá una coordenada x e y de (0, 0),
# y la esquina inferior derecha tendrá una coordenada x e y de (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Establezca las coordenadas de la esquina superior izquierda del grupo en (-250, -250).
# El centro del grupo ahora tendrá un valor de coordenada x e y de (0, 0),
# y la esquina inferior derecha estará en (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Cree un rectángulo que mostrará el límite de este grupo de formas y añádalo al grupo.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Una vez que una forma es parte de un grupo de formas, podemos acceder a ella como un nodo hijo y luego modificarla.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Cree una pequeña estrella roja y insértela en el grupo.
# Alinea la forma con el origen de coordenadas del grupo, que hemos movido al centro.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Inserta un rectángulo y luego inserta un rectángulo ligeramente más pequeño en el mismo lugar con una imagen.
# Las formas más nuevas que añadimos al grupo se superponen a las formas más antiguas. El rectángulo azul claro se superpondrá parcialmente a la estrella roja,
# y luego la forma con la imagen se superpondrá al rectángulo azul claro, usándolo como marco.
# No podemos usar las propiedades "ZOrder" de las formas para manipular su disposición dentro de una forma de grupo.
child3 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child3.width = 250
child3.height = 250
child3.left = -250
child3.top = -250
child3.fill_color = aspose.pydrawing.Color.light_blue
group.append_child(child3)
child4 = aw.drawing.Shape(doc, aw.drawing.ShapeType.IMAGE)
child4.width = 200
child4.height = 200
child4.left = -225
child4.top = -225
group.append_child(child4)
group.get_child(aw.NodeType.SHAPE, 3, True).as_shape().image_data.set_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Inserta un cuadro de texto en la forma de grupo. Establece la propiedad "Left" para que el borde derecho del cuadro de texto
# toque el límite derecho de la forma de grupo. Establece la propiedad "Top" para que el cuadro de texto quede fuera
# del límite de la forma de grupo, alineando su parte superior a lo largo del margen inferior de la forma de grupo.
child5 = aw.drawing.Shape(doc, aw.drawing.ShapeType.TEXT_BOX)
child5.width = 200
child5.height = 50
child5.left = group.coord_size.width + group.coord_origin.x - 200
child5.top = group.coord_size.height + group.coord_origin.y
group.append_child(child5)
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(group)
builder.move_to(group.get_child(aw.NodeType.SHAPE, 4, True).as_shape().append_child(aw.Paragraph(doc)))
builder.write('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'Shape.GroupShape.docx')
```

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

