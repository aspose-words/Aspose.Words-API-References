---
title: DefaultFontSubstitutionRule.default_font_name property
linktitle: default_font_name property
articleTitle: default_font_name property
second_title: Aspose.Words for Python
description: "DefaultFontSubstitutionRule.default_font_name property. Gets or sets the default font name."
type: docs
weight: 10
url: /sv/python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
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
# Teckensnittskällorna som dokumentet använder innehåller teckensnittet "Arial", men inte "Arvo".
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# Ställ in egenskapen "DefaultFontName" till "Courier New" för att,
# vid rendering av dokumentet, använd det teckensnittet i alla fall när ett annat teckensnitt inte är tillgängligt.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Aspose.Words kommer nu att använda standardteckensnittet i stället för saknade teckensnitt under alla renderingsanrop.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontName.pdf')
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Hämta standardsubstitutionsregeln i FontSettings.
# Denna regel kommer att ersätta alla saknade teckensnitt med "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# Ställ in standardteckensnittsersättningen till "Courier New".
default_font_substitution_rule.default_font_name = 'Courier New'
# Med en dokumentbyggare, lägg till lite text i ett teckensnitt som vi inte har för att se substitutionen ske,
# och rendera sedan resultatet i en PDF.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

