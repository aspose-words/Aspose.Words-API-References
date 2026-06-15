---
title: IWarningCallback class
linktitle: IWarningCallback class
articleTitle: IWarningCallback class
second_title: Aspose.Words for Python
description: "aspose.words.IWarningCallback class. Implement this interface if you want to have your own custom method called to  capture loss of fidelity warnings that can occur during document loading or saving."
type: docs
weight: 620
url: /python-net/aspose.words/iwarningcallback/
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
# Store the current collection of font sources, which will be the default font source for every document
# for which we do not specify a different font source.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# When rendering the document, there will be no place to find the "Times New Roman" font.
# This will cause a font substitution warning, which our callback will detect.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Open a document that contains text formatted with a font that does not exist in any of our font sources.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Assign a callback for handling font substitution warnings.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Set a default font name and enable font substitution.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Original font metrics should be used after font substitution.
doc.layout_options.keep_original_font_metrics = True
# We will get a font substitution warning if we save a document with a missing font.
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
# Set the "EmulateRasterOperations" property to "false" to fall back to bitmap when
# it encounters a metafile, which will require raster operations to render in the output PDF.
metafile_rendering_options.emulate_raster_operations = False
# Set the "RenderingMode" property to "VectorWithFallback" to try to render every metafile using vector graphics.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF and applies the configuration
# in our MetafileRenderingOptions object to the saving operation.
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

