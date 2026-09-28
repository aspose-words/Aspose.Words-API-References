---
title: SaveOptions.iml_rendering_mode property
linktitle: iml_rendering_mode property
articleTitle: iml_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.iml_rendering_mode property. Gets or sets a value determining how ink (InkML) objects are rendered."
type: docs
weight: 70
url: /zh/python-net/aspose.words.saving/saveoptions/iml_rendering_mode/
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
# 将 'ImlRenderingMode.InkML' 设置为忽略墨水（InkML）对象的回退形状并直接渲染 InkML 本身。
# 如果渲染结果不令人满意，
# 请使用 'ImlRenderingMode.Fallback' 以获得类似于以前版本的结果。
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
save_options.iml_rendering_mode = aw.saving.ImlRenderingMode.INK_ML
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.RenderInkObject.jpeg', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

