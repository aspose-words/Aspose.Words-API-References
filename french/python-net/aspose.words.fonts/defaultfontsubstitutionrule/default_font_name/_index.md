---
title: DefaultFontSubstitutionRule.default_font_name property
linktitle: default_font_name property
articleTitle: default_font_name property
second_title: Aspose.Words for Python
description: "DefaultFontSubstitutionRule.default_font_name property. Gets or sets the default font name."
type: docs
weight: 10
url: /fr/python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
---

## DefaultFontSubstitutionRule.default_font_name property

Gets or sets the default font name.


```python
@property
def default_font_name(self) -> str:
    ...

@default_font_name.setter
def default_font_name(self, value: str):
    ...

```

### Remarks

The default value is 'Times New Roman'.




### Examples

Shows how to specify a default font.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Arvo'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Les sources de polices utilisées par le document contiennent la police "Arial", mais pas "Arvo".
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# Définissez la propriété "DefaultFontName" sur "Courier New" pour,
# lors du rendu du document, appliquez cette police dans tous les cas lorsqu'une autre police n'est pas disponible.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Aspose.Words utilisera désormais la police par défaut à la place de toute police manquante lors de tout appel de rendu.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontName.pdf')
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Obtenez la règle de substitution par défaut dans FontSettings.
# Cette règle remplacera toutes les polices manquantes par "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# Définissez le substitut de police par défaut sur "Courier New".
default_font_substitution_rule.default_font_name = 'Courier New'
# En utilisant un constructeur de document, ajoutez du texte dans une police que nous ne possédons pas pour voir la substitution se produire,
# et puis rendez le résultat en PDF.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

