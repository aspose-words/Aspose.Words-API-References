---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /python-net/aspose.words/document/font_settings/
---

## Document.font_settings property

Gets or sets document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

This property allows to specify font settings per document. If set to ``None``, default static font settings
[FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# The default font sources contain the first font that the document uses.
self.assertEqual(1, len(font_sources))
self.assertTrue(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Arial')))
# The second font, "Amethysta", is unavailable.
self.assertFalse(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Amethysta')))
# We can configure a font substitution table which determines
# which fonts Aspose.Words will use as substitutes for unavailable fonts.
# Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
# If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
self.assertFalse(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Arvo')))
# "Arvo" is also unavailable, but "Courier New" is.
self.assertTrue(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Courier New')))
# The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
doc.save(ARTIFACTS_DIR + 'FontSettings.table_substitution.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

