---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /ar/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# أدخل شكلاً. إذا فتحنا هذا المستند في Microsoft Word، يمكننا النقر بزر الفأرة الأيسر على الشكل للكشف عنه
# ثمانية مقابض لتغيير الحجم حول محيطه، يمكننا النقر عليها وسحبها لتغيير حجمه.
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# اضبط الخاصية "AspectRatioLocked" إلى "true" للحفاظ على نسبة أبعاد الشكل
# عند استخدام أي من المقابض الأربعة القطرية لتغيير الحجم، التي تغير كلًا من ارتفاع الصورة وعرضها.
# استخدام أي من مقابض الحجم العمودية التي تغير إما الارتفاع أو العرض سيظل يغيّر نسبة الأبعاد.
# اضبط الخاصية "AspectRatioLocked" إلى "false" للسماح لنا بـ
# تغيير نسبة أبعاد الصورة بحرية باستخدام جميع مقابض الحجم.
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

