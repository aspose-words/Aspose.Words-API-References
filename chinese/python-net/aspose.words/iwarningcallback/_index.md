---
title: IWarningCallback class
linktitle: IWarningCallback class
articleTitle: IWarningCallback class
second_title: Aspose.Words for Python
description: "aspose.words.IWarningCallback class. Implement this interface if you want to have your own custom method called to  capture loss of fidelity warnings that can occur during document loading or saving."
type: docs
weight: 620
url: /zh/python-net/aspose.words/iwarningcallback/
---

## IWarningCallback class

Implement this interface if you want to have your own custom method called to 
capture loss of fidelity warnings that can occur during document loading or saving.


### Methods

| Name | Description |
| --- | --- |
|[ warning(info)](./warning/#warninginfo) | Aspose.Words invokes this method when it encounters some issue during document loading  or saving that might result in loss of formatting or data fidelity. |

### Examples

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
callback = self.FontSubstitutionWarningCollector()
doc.warning_callback = callback
# 存储当前的字体源集合，这将成为每个文档的默认字体源
# 对于我们未指定其他字体源的情况。
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# 出于测试目的，我们将把 Aspose.Words 设置为仅在不存在的文件夹中查找字体。
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# 在渲染文档时，将找不到 \"Times New Roman\" 字体。
# 这将导致字体替换警告，我们的回调函数会检测到它。
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# 打开一个文档，其中包含使用我们任何字体源中不存在的字体格式化的文本。
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# 为处理字体替换警告分配回调函数。
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# 设置默认字体名称并启用字体替换。
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# 字体替换后应使用原始字体度量。
doc.layout_options.keep_original_font_metrics = True
# 如果我们保存的文档缺少字体，将会收到字体替换警告。
doc.font_settings = font_settings
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.EnableFontSubstitution.pdf')
for info in warning_collector:
    if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
        print(info.description)
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings (FontSubstitutionWarningCollector).

```python
class FontSubstitutionWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
            self.font_substitution_warnings.warning(info)
```

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

* module [aspose.words](../)

