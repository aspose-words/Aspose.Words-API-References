---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /sv/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# Infoga en form. Om vi öppnar det här dokumentet i Microsoft Word kan vi vänsterklicka på formen för att avslöja
# åtta storlekshandtag runt dess omkrets, som vi kan klicka och dra för att ändra dess storlek.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Ställ in egenskapen "AspectRatioLocked" till "true" för att bevara formens bildförhållande
# när du använder något av de fyra diagonala storlekshandtagen, som ändrar både bildens höjd och bredd.
# Att använda någon ortogonal storlekshandtag som antingen ändrar höjden eller bredden kommer fortfarande att ändra bildförhållandet.
# Ställ in egenskapen "AspectRatioLocked" till "false" för att låta oss
# fritt ändra bildens bildförhållande med alla storlekshandtag.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

