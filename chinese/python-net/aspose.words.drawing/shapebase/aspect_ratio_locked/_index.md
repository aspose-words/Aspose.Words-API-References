---
title: ShapeBase.aspect_ratio_locked property
linktitle: aspect_ratio_locked property
articleTitle: aspect_ratio_locked property
second_title: Aspose.Words for Python
description: "ShapeBase.aspect_ratio_locked property. Specifies whether the shape's aspect ratio is locked."
type: docs
weight: 40
url: /zh/python-net/aspose.words.drawing/shapebase/aspect_ratio_locked/
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
# 插入形状。如果我们在 Microsoft Word 中打开此文档，可以左键单击该形状以显示
# 其周围有八个大小控制手柄，我们可以点击并拖动它们来改变大小。
shape = builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
# 将 "AspectRatioLocked" 属性设置为 "true" 以保留形状的宽高比
# 当使用四个对角大小控制手柄时，会同时改变图像的高度和宽度。
# 使用任何正交大小控制手柄（仅改变高度或宽度）仍会改变宽高比。
# 将 "AspectRatioLocked" 属性设置为 "false" 以允许我们
# 使用所有大小控制手柄自由改变图像的宽高比。
shape.aspect_ratio_locked = lock_aspect_ratio
doc.save(file_name=ARTIFACTS_DIR + 'Shape.AspectRatio.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

