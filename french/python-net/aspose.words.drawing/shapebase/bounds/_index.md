---
title: ShapeBase.bounds property
linktitle: bounds property
articleTitle: bounds property
second_title: Aspose.Words for Python
description: "ShapeBase.bounds property. Gets or sets the location and size of the containing block of the shape."
type: docs
weight: 70
url: /fr/python-net/aspose.words.drawing/shapebase/bounds/
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
# Créez une forme groupée. Une forme groupée peut afficher une collection de nœuds de forme enfants.
# Dans Microsoft Word, cliquer à l'intérieur de la bordure de la forme groupée ou sur l'une des formes enfants de la forme groupée va
# sélectionner toutes les autres formes enfants de ce groupe et nous permettre de mettre à l'échelle et de déplacer toutes les formes en même temps.
group = aw.drawing.GroupShape(doc)
self.assertEqual(aw.drawing.WrapType.NONE, group.wrap_type)
# Créez une forme groupée de 400 pt x 400 pt et placez‑la à l'origine des coordonnées de forme flottante du document.
group.bounds = aspose.pydrawing.RectangleF(0, 0, 400, 400)
# Définissez la taille du plan de coordonnées interne du groupe à 500 x 500 pt.
# Le coin supérieur gauche du groupe aura des coordonnées x et y de (0, 0),
# et le coin inférieur droit aura des coordonnées x et y de (500, 500).
group.coord_size = aspose.pydrawing.Size(500, 500)
# Définissez les coordonnées du coin supérieur gauche du groupe à (-250, -250).
# Le centre du groupe aura maintenant une valeur de coordonnées x et y de (0, 0),
# et le coin inférieur droit sera à (250, 250).
group.coord_origin = aspose.pydrawing.Point(-250, -250)
# Créez un rectangle qui affichera la frontière de cette forme groupée et ajoutez‑le au groupe.
child1 = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
child1.width = group.coord_size.width
child1.height = group.coord_size.height
child1.left = group.coord_origin.x
child1.top = group.coord_origin.y
group.append_child(child1)
# Une fois qu'une forme fait partie d'une forme groupée, nous pouvons y accéder en tant que nœud enfant puis la modifier.
group.get_child(aw.NodeType.SHAPE, 0, True).as_shape().stroke.dash_style = aw.drawing.DashStyle.DASH
# Créez une petite étoile rouge et insérez‑la dans le groupe.
# Alignez la forme avec l'origine des coordonnées du groupe, que nous avons déplacée au centre.
child2 = aw.drawing.Shape(doc, aw.drawing.ShapeType.STAR)
child2.width = 20
child2.height = 20
child2.left = -10
child2.top = -10
child2.fill_color = aspose.pydrawing.Color.red
group.append_child(child2)
# Insérez un rectangle, puis insérez un rectangle légèrement plus petit au même endroit avec une image.
# Les formes plus récentes que nous ajoutons au groupe se superposent aux formes plus anciennes. Le rectangle bleu clair chevauchera partiellement l'étoile rouge,
# et ensuite la forme avec l'image chevauchera le rectangle bleu clair, en l'utilisant comme cadre.
# Nous ne pouvons pas utiliser les propriétés \"ZOrder\" des formes pour manipuler leur agencement au sein d'une forme groupée.
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
# Insérez une zone de texte dans la forme groupée. Définissez la propriété \"Left\" afin que le bord droit de la zone de texte
# touche la bordure droite de la forme groupée. Définissez la propriété \"Top\" afin que la zone de texte se situe à l'extérieur
# de la bordure de la forme groupée, avec sa taille supérieure alignée le long de la marge inférieure de la forme groupée.
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
# Même si la ligne elle-même occupe peu d'espace sur la page du document,
# elle occupe un bloc conteneur rectangulaire, dont la taille peut être déterminée à l'aide des propriétés \"Bounds\".
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds)
self.assertEqual(aspose.pydrawing.RectangleF(50, 50, 100, 100), shape.bounds_in_points)
# Créez une forme groupée, puis définissez la taille de son bloc conteneur à l'aide de la propriété \"Bounds\".
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(0, 100, 250, 250)
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
# Créez un rectangle, vérifiez la taille de son bloc de délimitation, puis ajoutez-le à la forme groupée.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 700
shape.top = 700
self.assertEqual(aspose.pydrawing.RectangleF(700, 700, 100, 100), shape.bounds_in_points)
group.append_child(shape)
# Le plan de coordonnées de la forme groupée a son origine dans le coin supérieur gauche de son bloc conteneur,
# et les coordonnées x et y de (1000, 1000) dans le coin inférieur droit.
# Notre forme groupée mesure 250 x 250 pt, donc chaque 4 pt sur le plan de coordonnées de la forme groupée
# correspond à 1 pt dans le plan de coordonnées du corps du document.
# Chaque forme que nous insérons rétrécira également de taille d'un facteur de 4.
# Le changement de la propriété \"BoundsInPoints\" de la forme reflétera cela.
self.assertEqual(aspose.pydrawing.RectangleF(175, 275, 25, 25), shape.bounds_in_points)
doc.first_section.body.first_paragraph.append_child(group)
# Insérez une forme et placez‑la en dehors des limites du bloc conteneur de la forme groupée.
shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.RECTANGLE)
shape.width = 100
shape.height = 100
shape.left = 1000
shape.top = 1000
group.append_child(shape)
# L'empreinte de la forme groupée dans le corps du document a augmenté, mais le bloc conteneur reste le même.
self.assertEqual(aspose.pydrawing.RectangleF(0, 100, 250, 250), group.bounds_in_points)
self.assertEqual(aspose.pydrawing.RectangleF(250, 350, 25, 25), shape.bounds_in_points)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.Bounds.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

