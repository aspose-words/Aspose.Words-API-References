---
title: MetafileRenderingOptions.rendering_mode property
linktitle: rendering_mode property
articleTitle: rendering_mode property
second_title: Aspose.Words for Python
description: "MetafileRenderingOptions.rendering_mode property. Gets or sets a value determining how metafile images should be rendered."
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/metafilerenderingoptions/rendering_mode/
---

## MetafileRenderingOptions.rendering_mode property

Gets or sets a value determining how metafile images should be rendered.


```python
@property
def rendering_mode(self) -> aspose.words.saving.MetafileRenderingMode:
    ...

@rendering_mode.setter
def rendering_mode(self, value: aspose.words.saving.MetafileRenderingMode):
    ...

```

### Remarks

The default value depends on the save format. For images it is [MetafileRenderingMode.BITMAP](../../metafilerenderingmode/#BITMAP).
For other formats it is [MetafileRenderingMode.VECTOR_WITH_FALLBACK](../../metafilerenderingmode/#VECTOR_WITH_FALLBACK).




### Examples

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records.

```python
doc = aw.Document(file_name=MY_DIR + 'WMF with image.docx')
metafile_rendering_options = aw.saving.MetafileRenderingOptions()
# 将 \"EmulateRasterOperations\" 属性设置为 \"false\"，以在
# 遇到元文件时回退到位图，因为在输出 PDF 中渲染需要光栅操作。
metafile_rendering_options.emulate_raster_operations = False
# 将 \"RenderingMode\" 属性设置为 \"VectorWithFallback\"，尝试使用矢量图形渲染每个元文件。
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 并应用配置的方式
# 在我们的 MetafileRenderingOptions 对象中用于保存操作。
save_options = aw.saving.PdfSaveOptions()
save_options.metafile_rendering_options = metafile_rendering_options
callback = self.HandleDocumentWarnings()
doc.warning_callback = callback
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.HandleBinaryRasterWarnings.pdf', save_options=save_options)
self.assertEqual(1, callback.warnings.count)
self.assertEqual("'R2_XORPEN' binary raster operation is not supported.", callback.warnings[0].description)
```

Shows added a fallback to bitmap rendering and changing type of warnings about unsupported metafile records (HandleDocumentWarnings).

```python
class HandleDocumentWarnings(aw.IWarningCallback):

    def __init__(self):
        self.warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.MINOR_FORMATTING_LOSS:
            print('Unsupported operation: ' + info.description)
            self.warnings.warning(info)
```

### See Also

* module [aspose.words.saving](../../)
* class [MetafileRenderingOptions](../)

