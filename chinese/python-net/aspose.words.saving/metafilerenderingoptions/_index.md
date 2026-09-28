---
title: MetafileRenderingOptions class
linktitle: MetafileRenderingOptions class
articleTitle: MetafileRenderingOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.MetafileRenderingOptions class. Allows to specify additional metafile rendering options"
type: docs
weight: 500
url: /zh/python-net/aspose.words.saving/metafilerenderingoptions/
---

## MetafileRenderingOptions class

Allows to specify additional metafile rendering options.
To learn more, visit the [Handling Windows Metafiles](https://docs.aspose.com/words/python-net/handling-windows-metafiles/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [MetafileRenderingOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [emf_plus_dual_rendering_mode](./emf_plus_dual_rendering_mode/) | Gets or sets a value determining how EMF+ Dual metafiles should be rendered. |
| [emulate_raster_operations](./emulate_raster_operations/) | Gets or sets a value determining whether or not the raster operations should be emulated. |
| [emulate_rendering_to_size_on_page](./emulate_rendering_to_size_on_page/) | Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size. |
| [emulate_rendering_to_size_on_page_resolution](./emulate_rendering_to_size_on_page_resolution/) | Gets or sets the resolution in pixels per inch for the emulation of metafile rendering to the size on page. |
| [rendering_mode](./rendering_mode/) | Gets or sets a value determining how metafile images should be rendered. |
| [use_emf_embedded_to_wmf](./use_emf_embedded_to_wmf/) | Gets or sets a value determining how WMF metafiles with embedded EMF metafiles should be rendered. |
| [use_gdi_raster_operations_emulation](./use_gdi_raster_operations_emulation/) | Gets or sets a value determining whether or not to use the GDI+ for raster operations emulation. |

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

* module [aspose.words.saving](../)

