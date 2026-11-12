---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /tr/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# Bir şekil ekleyin. Bu belgeyi Microsoft Word'de açarsak, şekle sol tıklayarak ortaya çıkarabiliriz.
# çevresinde sekiz boyutlandırma tutamağı, bunlara tıklayıp sürükleyerek boyutunu değiştirebiliriz.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# "AspectRatioLocked" özelliğini "true" olarak ayarlayarak şeklin en-boy oranını koruyun
# dört diyagonal boyutlandırma tutamacından herhangi birini kullandığınızda, bu tutamacılar görüntünün yüksekliğini ve genişliğini birlikte değiştirir.
# Yüksekliği ya da genişliği değiştiren herhangi bir ortogonal boyutlandırma tutamacını kullanmak hâlâ en-boy oranını değiştirecektir.
# "AspectRatioLocked" özelliğini "false" olarak ayarlayarak bize izin verin
# tüm boyutlandırma tutamacılarını kullanarak görüntünün en-boy oranını serbestçe değiştirebilirsiniz.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

