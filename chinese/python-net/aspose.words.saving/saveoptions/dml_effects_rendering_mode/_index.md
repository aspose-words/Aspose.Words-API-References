---
title: SaveOptions.dml_effects_rendering_mode property
linktitle: dml_effects_rendering_mode property
articleTitle: dml_effects_rendering_mode property
second_title: Aspose.Words for Python
description: "SaveOptions.dml_effects_rendering_mode property. Gets or sets a value determining how DrawingML effects are rendered."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/saveoptions/dml_effects_rendering_mode/
---

## SaveOptions.dml_effects_rendering_mode property

Gets or sets a value determining how DrawingML effects are rendered.


```python
@property
def dml_effects_rendering_mode(self) -> aspose.words.saving.DmlEffectsRenderingMode:
    ...

@dml_effects_rendering_mode.setter
def dml_effects_rendering_mode(self, value: aspose.words.saving.DmlEffectsRenderingMode):
    ...

```

### Remarks

The default value is [DmlEffectsRenderingMode.SIMPLIFIED](../../dmleffectsrenderingmode/#SIMPLIFIED).
This property is used when the document is exported to fixed page formats.




### Examples

Shows how to configure the rendering quality of DrawingML effects in a document as we save it to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'DrawingML shape effects.docx')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 将 "DmlEffectsRenderingMode" 属性设置为 "DmlEffectsRenderingMode.None" 以丢弃所有 DrawingML 效果。
# 将 "DmlEffectsRenderingMode" 属性设置为 "DmlEffectsRenderingMode.Simplified"
# 以渲染简化版的 DrawingML 效果。
# 将 "DmlEffectsRenderingMode" 属性设置为 "DmlEffectsRenderingMode.Fine" 以
# 更准确地渲染 DrawingML 效果，同时增加更多的处理成本。
options.dml_effects_rendering_mode = effects_rendering_mode
self.assertEqual(aw.saving.DmlRenderingMode.DRAWING_ML, options.dml_rendering_mode)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.DrawingMLEffects.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

