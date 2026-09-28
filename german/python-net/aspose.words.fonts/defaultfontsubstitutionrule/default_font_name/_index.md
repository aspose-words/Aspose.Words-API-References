---
title: DefaultFontSubstitutionRule.default_font_name property
linktitle: default_font_name property
articleTitle: default_font_name property
second_title: Aspose.Words for Python
description: "DefaultFontSubstitutionRule.default_font_name property. Gets or sets the default font name."
type: docs
weight: 10
url: /de/python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
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
# Die Schriftquellen, die das Dokument verwendet, enthalten die Schriftart "Arial", jedoch nicht "Arvo".
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# Setzen Sie die Eigenschaft "DefaultFontName" auf "Courier New", um
# während das Dokument gerendert wird, diese Schriftart in allen Fällen anzuwenden, wenn eine andere Schriftart nicht verfügbar ist.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Aspose.Words verwendet nun die Standardschriftart anstelle fehlender Schriftarten bei allen Rendering-Aufrufen.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontName.pdf')
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# Rufen Sie die Standard-Substitutionsregel innerhalb von FontSettings ab.
# Diese Regel ersetzt alle fehlenden Schriften durch "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual('Times New Roman', default_font_substitution_rule.default_font_name)
# Setzen Sie den Standard-Schriftart-Ersatz auf "Courier New".
default_font_substitution_rule.default_font_name = 'Courier New'
# Verwenden Sie einen Document Builder, fügen Sie Text in einer Schriftart hinzu, die wir nicht besitzen, um die Substitution zu beobachten,
# und rendern Sie anschließend das Ergebnis in ein PDF.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Missing Font'
builder.writeln('Line written in a missing font, which will be substituted with Courier New.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontSubstitutionRule.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

