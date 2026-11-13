---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /es/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# Inserte una forma. Si abrimos este documento en Microsoft Word, podemos hacer clic izquierdo en la forma para revelar
# ocho controladores de tamaño alrededor de su perímetro, que podemos hacer clic y arrastrar para cambiar su tamaño.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Establezca la propiedad "AspectRatioLocked" a "true" para preservar la relación de aspecto de la forma
# al usar cualquiera de los cuatro controladores de tamaño diagonales, que cambian tanto la altura como el ancho de la imagen.
# Usar cualquier controlador de tamaño ortogonal que cambie la altura o el ancho seguirá modificando la relación de aspecto.
# Establezca la propiedad "AspectRatioLocked" a "false" para permitirnos
# cambiar libremente la relación de aspecto de la imagen con todos los controladores de tamaño.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

