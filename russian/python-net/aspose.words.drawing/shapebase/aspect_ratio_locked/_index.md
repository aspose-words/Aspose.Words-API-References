---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /ru/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# Вставьте форму. Если открыть этот документ в Microsoft Word, мы можем щелкнуть левой кнопкой мыши по форме, чтобы отобразить
# восемь маркеров изменения размера вокруг её периметра, которые мы можем щёлкнуть и перетащить, чтобы изменить её размер.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# Установите свойство "AspectRatioLocked" в значение "true", чтобы сохранить соотношение сторон формы
# при использовании любого из четырёх диагональных маркеров изменения размера, которые изменяют как высоту, так и ширину изображения.
# Использование любых ортогональных маркеров изменения размера, которые изменяют либо высоту, либо ширину, всё равно изменит соотношение сторон.
# Установите свойство "AspectRatioLocked" в значение "false", чтобы позволить нам
# свободно изменять соотношение сторон изображения всеми маркерами изменения размера.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

