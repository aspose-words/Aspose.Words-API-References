---
title: DmlEffectsRenderingMode enumeration
linktitle: DmlEffectsRenderingMode enumeration
articleTitle: DmlEffectsRenderingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.DmlEffectsRenderingMode enumeration. Specifies how DrawingML effects are rendered to fixed page formats."
type: docs
weight: 80
url: /zh/python-net/aspose.words.saving/dmleffectsrenderingmode/
---

## DmlEffectsRenderingMode enumeration

Specifies how DrawingML effects are rendered to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| SIMPLIFIED | Rendering of DrawingML effects are simplified. |
| NONE | No DrawingML effects are rendered. |
| FINE | DrawingML effects are rendered in fine mode which involves advanced processing. In this mode rendering of effects gives better results but at a higher performance cost than [DmlEffectsRenderingMode.SIMPLIFIED](./#SIMPLIFIED) mode. |

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

* module [aspose.words.saving](../)

