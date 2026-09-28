---
title: ShapeBase.coord_size property
linktitle: coord_size property
articleTitle: coord_size property
second_title: Aspose.Words for Python
description: "ShapeBase.coord_size property. The width and height of the coordinate space inside the containing block of this shape."
type: docs
weight: 120
url: /fr/python-net/aspose.words.drawing/shapebase/coord_size/
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

Shows how to translate the x and y coordinate location on a shape's coordinate plane to a location on the parent shape's coordinate plane.

```python
doc = aw.Document()
# Insérez une forme groupée, et placez‑la 100 points en dessous et à droite de
# le point d'origine des coordonnées x et Y du document.
group = aw.drawing.GroupShape(doc)
group.bounds = aspose.pydrawing.RectangleF(100, 100, 500, 500)
# Utilisez la méthode "LocalToParent" pour déterminer que (0, 0) sur les coordonnées x et y internes du groupe
# se trouve à (100, 100) du système de coordonnées de sa forme parente. Le parent de la forme groupée est le document lui‑même.
self.assertEqual(aspose.pydrawing.PointF(100, 100), group.local_to_parent(aspose.pydrawing.PointF(0, 0)))
# Par défaut, le plan de coordonnées interne d'une forme a le coin supérieur gauche à (0, 0),
# et le coin inférieur droit à (1000, 1000). En raison de sa taille, notre forme groupée couvre une zone de 500pt x 500pt
# dans le plan du document. Cela signifie qu'un déplacement de 1pt sur le plan de coordonnées du document se traduira
# par un déplacement de 2pt sur le plan de coordonnées de la forme groupée.
self.assertEqual(aspose.pydrawing.PointF(150, 150), group.local_to_parent(aspose.pydrawing.PointF(100, 100)))
self.assertEqual(aspose.pydrawing.PointF(200, 200), group.local_to_parent(aspose.pydrawing.PointF(200, 200)))
self.assertEqual(aspose.pydrawing.PointF(250, 250), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Déplacez l'origine des axes x et y de la forme groupée du coin supérieur gauche vers le centre.
# Cela décalera davantage les coordonnées internes du groupe par rapport aux coordonnées du document.
group.coord_origin = aspose.pydrawing.Point(-250, -250)
self.assertEqual(aspose.pydrawing.PointF(375, 375), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Modifier l'échelle du plan de coordonnées affectera également les emplacements relatifs.
group.coord_size = aspose.pydrawing.Size(500, 500)
self.assertEqual(aspose.pydrawing.PointF(650, 650), group.local_to_parent(aspose.pydrawing.PointF(300, 300)))
# Si nous souhaitons ajouter une forme à ce groupe tout en définissant son emplacement à partir d'un emplacement dans le document,
# nous devrons d'abord confirmer un emplacement dans la forme groupée qui correspondra à l'emplacement du document.
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

