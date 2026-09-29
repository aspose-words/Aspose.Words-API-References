---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /it/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# Inserisci una forma. Se apriamo questo documento in Microsoft Word, possiamo fare clic con il tasto sinistro sulla forma per rivelare
# otto maniglie di ridimensionamento intorno al suo perimetro, che possiamo cliccare e trascinare per modificarne le dimensioni.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Imposta la proprietà "AspectRatioLocked" su "true" per preservare il rapporto d'aspetto della forma
# quando si usano una delle quattro maniglie di ridimensionamento diagonali, che modificano sia l'altezza che la larghezza dell'immagine.
# L'uso di qualsiasi maniglia di ridimensionamento ortogonale che modifica l'altezza o la larghezza cambierà comunque il rapporto d'aspetto.
# Imposta la proprietà "AspectRatioLocked" su "false" per permetterci di
# modificare liberamente il rapporto d'aspetto dell'immagine con tutte le maniglie di ridimensionamento.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

