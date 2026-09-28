---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /fr/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
---

## ShapeBase.aspect_ratio_locked property

Specifies whether the shape's aspect ratio is locked.


```python
@property
def aspect_ratio_locked(self) -> bool:
    ...

@aspect_ratio_locked.setter
def aspect_ratio_locked(self, value: bool):
    ...

```

### Remarks

The default value depends on the [ShapeType](../../shapetype/), for the [ShapeType.IMAGE](../../shapetype/#IMAGE) it is ``True``
but for the other shape types it is ``False``.

Has effect for top level shapes only.




### Examples

Shows how to lock/unlock a shape's aspect ratio.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérer une forme. Si nous ouvrons ce document dans Microsoft Word, nous pouvons cliquer gauche sur la forme pour révéler
# huit poignées de redimensionnement autour de son périmètre, que nous pouvons cliquer et faire glisser pour changer sa taille.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Définissez la propriété "AspectRatioLocked" sur "true" pour préserver le rapport d'aspect de la forme
# lors de l'utilisation de l'une des quatre poignées de redimensionnement diagonales, qui modifient à la fois la hauteur et la largeur de l'image.
# L'utilisation de n'importe quelle poignée de redimensionnement orthogonale qui modifie soit la hauteur, soit la largeur modifiera toujours le rapport d'aspect.
# Définissez la propriété "AspectRatioLocked" sur "false" pour nous permettre de
# modifier librement le rapport d'aspect de l'image avec toutes les poignées de redimensionnement.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

