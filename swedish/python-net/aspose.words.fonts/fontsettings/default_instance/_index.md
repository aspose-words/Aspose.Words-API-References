---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fonts/fontsettings/default_instance/
---

## FontSettings.default_instance property

Static default font settings.


```python
@property
def default_instance(self) -> aspose.words.fonts.FontSettings:
    ...

```

### Remarks

This instance is used by default in a document unless [Document.font_settings](../../../aspose.words/document/font_settings/) is specified.



### Examples

Shows how to configure the default font settings instance.

```python
# Konfigurera standardinstansen för teckensnittsinställningar att använda teckensnittet \"Courier New\"
# som en reservsubstitution när vi försöker använda ett okänt teckensnitt.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
# Detta dokument har ingen FontSettings-konfiguration. När vi renderar dokumentet,
# kommer standardinstansen för FontSettings att lösa det saknade teckensnittet.
# Aspose.Words kommer att använda \"Courier New\" för att rendera text som använder det okända teckensnittet.
self.assertIsNone(doc.font_settings)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontInstance.pdf')
```

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

Shows how to use the IWarningCallback interface to monitor font substitution warnings (FontSubstitutionWarningCollector).

```python
class FontSubstitutionWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
            self.font_substitution_warnings.warning(info)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

