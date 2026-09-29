---
title: IWarningCallback class
linktitle: IWarningCallback class
articleTitle: IWarningCallback class
second_title: Aspose.Words for Python
description: "aspose.words.IWarningCallback class. Implement this interface if you want to have your own custom method called to  capture loss of fidelity warnings that can occur during document loading or saving."
type: docs
weight: 620
url: /sv/python-net/aspose.words/iwarningcallback/
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
# Spara den aktuella samlingen av teckensnittskällor, som kommer att vara standardteckensnittskälla för varje dokument
# för vilka vi inte anger en annan teckensnittskälla.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# För teständamål kommer vi att ställa in Aspose.Words så att den bara söker efter teckensnitt i en mapp som inte finns.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# När dokumentet renderas kommer det inte finnas någon plats att hitta teckensnittet "Times New Roman".
# Detta kommer att orsaka en varning om teckensnittssubstitution, som vår återuppringning kommer att upptäcka.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```python
# Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
doc = aw.Document(file_name=MY_DIR + 'Missing font.docx')
# Tilldela en återuppringning för att hantera varningar om teckensnittsersättning.
warning_collector = aw.WarningInfoCollection()
doc.warning_callback = warning_collector
# Ange ett standardteckensnittsnamn och aktivera teckensnittsersättning.
font_settings = aw.fonts.FontSettings()
font_settings.substitution_settings.default_font_substitution.default_font_name = 'Arial'
font_settings.substitution_settings.font_info_substitution.enabled = True
# Ursprungliga teckensnittsmått bör användas efter teckensnittsersättning.
doc.layout_options.keep_original_font_metrics = True
# Vi får en varning om teckensnittsersättning om vi sparar ett dokument med ett saknat teckensnitt.
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
# Ställ in egenskapen "EmulateRasterOperations" till "false" för att falla tillbaka till bitmap när
# den stöter på en metafil, vilket kommer att kräva rasteroperationer för att rendera i den resulterande PDF:en.
metafile_rendering_options.emulate_raster_operations = False
# Ställ in egenskapen "RenderingMode" till "VectorWithFallback" för att försöka rendera varje metafil med vektorgrafik.
metafile_rendering_options.rendering_mode = aw.saving.MetafileRenderingMode.VECTOR_WITH_FALLBACK
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF och tillämpar konfigurationen
# i vårt MetafileRenderingOptions-objekt för sparningsoperationen.
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

