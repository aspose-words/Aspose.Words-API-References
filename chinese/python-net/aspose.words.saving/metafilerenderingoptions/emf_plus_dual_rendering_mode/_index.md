---
title: MetafileRenderingOptions.emf_plus_dual_rendering_mode property
linktitle: emf_plus_dual_rendering_mode property
articleTitle: emf_plus_dual_rendering_mode property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.emf_plus_dual_rendering_mode property. Gets or sets a value determining how EMF+ Dual metafiles should be rendered."
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/metafilerenderingoptions/emf_plus_dual_rendering_mode/
---

## MetafileRenderingOptions.emf_plus_dual_rendering_mode property

Gets or sets a value determining how EMF+ Dual metafiles should be rendered.


```python
@property
def emf_plus_dual_rendering_mode(self) -> aspose.words.saving.EmfPlusDualRenderingMode:
    ...

@emf_plus_dual_rendering_mode.setter
def emf_plus_dual_rendering_mode(self, value: aspose.words.saving.EmfPlusDualRenderingMode):
    ...

```

### Remarks

EMF+ Dual metafiles contains both EMF+ and EMF parts. MS Word and GDI+ always renders EMF+ part.
Aspose.Words currently doesn't fully supports all EMF+ records and in some cases rendering result of
EMF part looks better then rendering result of EMF+ part.

This option is used only when metafile is rendered as vector graphics. When metafile is rendered
to bitmap, EMF+ part is always used.

The default value is [EmfPlusDualRenderingMode.EMF_PLUS_WITH_FALLBACK](../../emfplusdualrenderingmode/#EMF_PLUS_WITH_FALLBACK).




### Examples

Shows how to configure Enhanced Windows Metafile-related rendering options when saving to PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'EMF.docx')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
# 将 "EmfPlusDualRenderingMode" 属性设置为 "EmfPlusDualRenderingMode.Emf"
# 仅渲染 EMF+ 双元文件的 EMF 部分。
# 将 "EmfPlusDualRenderingMode" 属性设置为 "EmfPlusDualRenderingMode.EmfPlus" 以
# 渲染 EMF+ 双元文件的 EMF+ 部分。
# 将 "EmfPlusDualRenderingMode" 属性设置为 "EmfPlusDualRenderingMode.EmfPlusWithFallback"
# 如果所有 EMF+ 记录均受支持，则渲染 EMF+ 双元文件的 EMF+ 部分。
# 否则，Aspose.Words 将渲染 EMF 部分。
save_options.metafile_rendering_options.emf_plus_dual_rendering_mode = rendering_mode
# 将 "UseEmfEmbeddedToWmf" 属性设置为 "true"，以渲染嵌入的 EMF 数据
# 用于我们可以将其渲染为矢量图形的元文件。
save_options.metafile_rendering_options.use_emf_embedded_to_wmf = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderMetafile.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

