---
title: ShapeBase.coord_origin property
linktitle: coord_origin property
articleTitle: coord_origin property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_origin property. The coordinates at the top-left corner of the containing block of this shape."
type: docs
weight: 110
url: /it/python-net/aspose.words.drawing/shapebase/coord_origin/
---

## ShapeBase.coord_origin property

The coordinates at the top-left corner of the containing block of this shape.


```python
@property
def coord_origin(self) -> aspose.pydrawing.Point:
    ...

@coord_origin.setter
def coord_origin(self, value: aspose.pydrawing.Point):
    ...

```

### Remarks

The default value is (0,0).




### Examples

Shows how to create and populate a group shape.

```python
doc = aw.Document()
# Crea una forma di gruppo. Una forma di gruppo può visualizzare una collezione di nodi di forma figlio.
# In Microsoft Word, fare clic all'interno del contorno della forma di gruppo o su una delle forme figlio della forma di gruppo farà
# selezionare tutte le altre forme figlio all'interno di questo gruppo e permetterci di scalare e spostare tutte le forme contemporaneamente.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Crea una forma di gruppo di 400pt x 400pt e posizionala all'origine delle coordinate della forma flottante del documento.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Imposta la dimensione del piano di coordinate interno del gruppo a 500 x 500pt.
# L'angolo in alto a sinistra del gruppo avrà una coordinata x e y di (0, 0),
# e l'angolo in basso a destra avrà una coordinata x e y di (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Imposta le coordinate dell'angolo in alto a sinistra del gruppo a (-250, -250).
# Il centro del gruppo avrà ora un valore di coordinata x e y di (0, 0),
# e l'angolo in basso a destra sarà a (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Crea un rettangolo che visualizzerà il contorno di questa forma di gruppo e aggiungilo al gruppo.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Una volta che una forma fa parte di una forma di gruppo, possiamo accedervi come nodo figlio e poi modificarla.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Crea una piccola stella rossa e inseriscila nel gruppo.
# Allinea la forma con l'origine delle coordinate del gruppo, che abbiamo spostato al centro.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Inserisci un rettangolo, quindi inserisci un rettangolo leggermente più piccolo nello stesso punto con un'immagine.
# Le forme più recenti che aggiungiamo al gruppo si sovrappongono alle forme più vecchie. Il rettangolo azzurro chiaro si sovrapporrà parzialmente alla stella rossa,
# e poi la forma con l'immagine si sovrapporrà al rettangolo azzurro chiaro, usandolo come cornice.
# Non possiamo usare le proprietà \"ZOrder\" delle forme per manipolare il loro ordine all'interno di una forma di gruppo.
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
# Inserisci una casella di testo nella forma di gruppo. Imposta la proprietà \"Left\" in modo che il bordo destro della casella di testo
# tocchi il confine destro della forma di gruppo. Imposta la proprietà \"Top\" in modo che la casella di testo si trovi al di fuori
# del confine della forma di gruppo, con la sua parte superiore allineata lungo il margine inferiore della forma di gruppo.
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
# Inserisci una forma di gruppo e posizionala 100 punti sotto e a destra di
# il punto di origine delle coordinate x e Y del documento.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Usa il metodo "LocalToParent" per determinare che (0, 0) sulle coordinate interne x e y del gruppo
# si trova su (100, 100) del sistema di coordinate della forma genitore. Il genitore della forma di gruppo è il documento stesso.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Per impostazione predefinita, il piano di coordinate interno di una forma ha l'angolo in alto a sinistra a (0, 0),
# e l'angolo in basso a destra a (1000, 1000). A causa delle sue dimensioni, la nostra forma di gruppo copre un'area di 500pt x 500pt
# nel piano del documento. Ciò significa che un movimento di 1pt sul piano di coordinate del documento verrà tradotto
# in un movimento di 2pt sul piano di coordinate della forma di gruppo.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Sposta l'origine degli assi x e y della forma di gruppo dall'angolo in alto a sinistra al centro.
# Questo sposterà ulteriormente le coordinate interne del gruppo rispetto a quelle del documento.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Modificare la scala del piano di coordinate influenzerà anche le posizioni relative.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Se desideriamo aggiungere una forma a questo gruppo definendo la sua posizione in base a una posizione nel documento,
# dovremo prima confermare una posizione nella forma di gruppo che corrisponda a quella del documento.
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

