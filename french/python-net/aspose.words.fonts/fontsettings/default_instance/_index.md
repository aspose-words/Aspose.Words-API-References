---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /fr/python-net/aspose.words.fonts/fontsettings/default_instance/
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
# Configurez l'instance des paramètres de police par défaut pour utiliser la police "Courier New"
# comme substitut de secours lorsque nous essayons d'utiliser une police inconnue.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
# Ce document n'a pas de configuration FontSettings. Lorsque nous rendons le document,
# l'instance par défaut de FontSettings résoudra la police manquante.
# Aspose.Words utilisera "Courier New" pour rendre le texte qui utilise la police inconnue.
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
# Enregistrez la collection actuelle de sources de polices, qui sera la source de police par défaut pour chaque document
# pour lequel nous ne spécifions pas une source de police différente.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# À des fins de test, nous définirons Aspose.Words pour rechercher les polices uniquement dans un dossier qui n'existe pas.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# Lors du rendu du document, il n'y aura aucun endroit où trouver la police "Times New Roman".
# Cela déclenchera un avertissement de substitution de police, que notre rappel détectera.
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

