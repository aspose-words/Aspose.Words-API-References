---
title: default_font_name property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the default font name."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/defaultfontsubstitutionrule/default_font_name/
---

## DefaultFontSubstitutionRule.default_font_name property

Gets or sets the default font name.

The default value is 'Times New Roman'.




### Examples

Shows how to specify a default font.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Arial"
builder.writeln("Hello world!")
builder.font.name = "Arvo"
builder.writeln("The quick brown fox jumps over the lazy dog.")

font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()

# The font sources that the document uses contain the font "Arial", but not "Arvo".
self.assertEqual(1, font_sources.length)
self.assertTrue(any(f for f in font_sources[0].get_available_fonts() if f.full_font_name == "Arial"))
self.assertFalse(any(f for f in font_sources[0].get_available_fonts() if f.full_font_name == "Arvo"))

# Set the "default_font_name" property to "Courier New" to,
# while rendering the document, apply that font in all cases when another font is not available.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = "Courier New"

self.assertTrue(any(f for f in font_sources[0].get_available_fonts() if f.full_font_name == "Courier New"))

# Aspose.Words will now use the default font in place of any missing fonts during any rendering calls.
doc.save(ARTIFACTS_DIR + "FontSettings.default_font_name.pdf")
```

Shows how to set the default font substitution rule.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings

# Get the default substitution rule within FontSettings.
# This rule will substitute all missing fonts with "Times New Roman".
default_font_substitution_rule = font_settings.substitution_settings.default_font_substitution
self.assertTrue(default_font_substitution_rule.enabled)
self.assertEqual("Times New Roman", default_font_substitution_rule.default_font_name)

# Set the default font substitute to "Courier New".
default_font_substitution_rule.default_font_name = "Courier New"

# Using a document builder, add some text in a font that we do not have to see the substitution take place,
# and then render the result in a PDF.
builder = aw.DocumentBuilder(doc)

builder.font.name = "Missing Font"
builder.writeln("Line written in a missing font, which will be substituted with Courier New.")

doc.save(ARTIFACTS_DIR + "FontSettings.default_font_substitution_rule.pdf")
```

### See Also

* module [aspose.words.fonts](../../)
* class [DefaultFontSubstitutionRule](../)

