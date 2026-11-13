---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /es/python-net/aspose.words.drawing/shapebase/coord_size/
---

## ShapeBase.coord_size property

The width and height of the coordinate space inside the containing block of this shape.


```python
@property
def coord_size(self) -> aspose.pydrawing.Size:
    ...

@coord_size.setter
def coord_size(self, value: aspose.pydrawing.Size):
    ...

```

### Remarks

The default value is (1000, 1000).




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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Inserte una forma de grupo y colóquela 100 puntos debajo y a la derecha de
# el punto de origen de coordenadas x y Y del documento.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Utilice el método "LocalToParent" para determinar que (0, 0) en las coordenadas internas x e y del grupo
# se encuentra en (100, 100) del sistema de coordenadas de su forma padre. El padre de la forma de grupo es el propio documento.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Por defecto, el plano de coordenadas interno de una forma tiene la esquina superior izquierda en (0, 0),
# y la esquina inferior derecha en (1000, 1000). Debido a su tamaño, nuestra forma de grupo cubre un área de 500pt x 500pt
# en el plano del documento. Esto significa que un movimiento de 1pt en el plano de coordenadas del documento se traducirá
# en un movimiento de 2pt en el plano de coordenadas de la forma de grupo.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Mueva el origen de los ejes x e y de la forma de grupo desde la esquina superior izquierda al centro.
# Esto desplazará aún más las coordenadas internas del grupo respecto a las coordenadas del documento.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Cambiar la escala del plano de coordenadas también afectará las ubicaciones relativas.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Si deseamos agregar una forma a este grupo mientras definimos su ubicación basándonos en una ubicación del documento,
# primero necesitaremos confirmar una ubicación en la forma de grupo que coincida con la ubicación del documento.
self.assertEqual(aspose.pydrawing.PointF(700, 700), group.local_to_parent(aspose.pydrawing.PointF(350, 350)))
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
group.append_child(shape)
doc.first_section.body.first_paragraph.append_child(group)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.LocalToParent.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

