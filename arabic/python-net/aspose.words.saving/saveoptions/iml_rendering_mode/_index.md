---
title: SaveOptions.iml_rendering_mode property
linktitle: iml_rendering_mode property
articleTitle: iml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.iml_rendering_mode property. Gets or sets a value determining how ink (InkML) objects are rendered."
type: docs
weight: 70
url: /ar/python-net/aspose.words.saving/saveoptions/iml_rendering_mode/
---

## SaveOptions.iml_rendering_mode property

Gets or sets a value determining how ink (InkML) objects are rendered.


```python
@property
def iml_rendering_mode(self) -> aspose.words.saving.ImlRenderingMode:
    ...

@iml_rendering_mode.setter
def iml_rendering_mode(self, value: aspose.words.saving.ImlRenderingMode):
    ...

```

### Remarks

The default value is [ImlRenderingMode.INK_ML](../../imlrenderingmode/#INK_ML).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to render Ink object.

```python
doc = aw.Document(file_name=MY_DIR + 'Ink object.docx')
# تعيين 'ImlRenderingMode.InkML' يتجاهل الشكل الاحتياطي لكائن الحبر (InkML) ويعرض InkML نفسه.
# إذا كانت نتيجة العرض غير مرضية،
# يرجى استخدام 'ImlRenderingMode.Fallback' للحصول على نتيجة مشابهة للإصدارات السابقة.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
save_options.iml_rendering_mode = aw.saving.ImlRenderingMode.INK_ML
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.RenderInkObject.jpeg', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

