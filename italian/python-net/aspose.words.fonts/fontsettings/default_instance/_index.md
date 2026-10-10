---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /it/python-net/aspose.words.fonts/fontsettings/default_instance/
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
# Configura l'istanza delle impostazioni di carattere predefinite per utilizzare il carattere "Courier New"
# come sostituto di backup quando tentiamo di utilizzare un carattere sconosciuto.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
# Questo documento non ha una configurazione FontSettings. Quando renderizziamo il documento,
# l'istanza predefinita di FontSettings risolverà il carattere mancante.
# Aspose.Words utilizzerà "Courier New" per renderizzare il testo che utilizza il carattere sconosciuto.
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
# Memorizza la raccolta corrente di font source, che sarà la fonte di font predefinita per ogni documento
# per i quali non specifichiamo una fonte di font diversa.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Per scopi di test, imposteremo Aspose.Words per cercare i font solo in una cartella che non esiste.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# Durante il rendering del documento, non ci sarà alcun posto dove trovare il font "Times New Roman".
# Ciò provocherà un avviso di sostituzione del font, che il nostro callback rileverà.
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

