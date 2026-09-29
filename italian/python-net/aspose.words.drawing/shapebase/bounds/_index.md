---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /it/python-net/aspose.words.drawing/shapebase/bounds/
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

Shows how to verify shape containing block boundaries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.LINE, horz_pos=aw.drawing.RelativeHorizontalPosition.LEFT_MARGIN, left=50, vert_pos=aw.drawing.RelativeVerticalPosition.TOP_MARGIN, top=50, width=100, height=100, wrap_type=aw.drawing.WrapType.NONE)
shape.stroke_color = aspose.pydrawing.Color.orange
# Anche se la linea stessa occupa poco spazio nella pagina del documento,
# occupa un blocco rettangolare contenitore, la cui dimensione possiamo determinare usando le proprietà \"Bounds\".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Crea una forma di gruppo, quindi imposta la dimensione del suo blocco contenitore usando la proprietà \"Bounds\".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Crea un rettangolo, verifica la dimensione del suo blocco di delimitazione, e poi aggiungilo alla forma di gruppo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Il piano di coordinate della forma di gruppo ha la sua origine nell'angolo in alto a sinistra del suo blocco contenitore,
# e le coordinate x e y di (1000, 1000) nell'angolo in basso a destra.
# La nostra forma di gruppo misura 250x250pt, quindi ogni 4pt sul piano di coordinate della forma di gruppo
# corrisponde a 1pt nel piano di coordinate del corpo del documento.
# Ogni forma che inseriamo si ridurrà anche di dimensione di un fattore 4.
# La modifica nella proprietà \"BoundsInPoints\" della forma rifletterà questo.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Inserisci una forma e posizionala al di fuori dei limiti del blocco contenitore della forma di gruppo.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# L'impronta della forma di gruppo nel corpo del documento è aumentata, ma il blocco contenitore rimane lo stesso.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

