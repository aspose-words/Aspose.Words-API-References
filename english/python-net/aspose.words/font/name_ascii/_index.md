---
title: name_ascii property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127)."
type: docs
weight: 240
url: /python-net/aspose.words/font/name_ascii/
---

## Font.name_ascii property

Returns or sets the font used for Latin text (characters with character codes from 0 (zero) through 127).


### Examples

Shows how Microsoft Word can combine two different fonts in one run.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Suppose a run that we use the builder to insert while using this font configuration
# contains characters within the ASCII characters' range. In that case,
# it will display those characters using this font.
builder.font.name_ascii = "Calibri"

# With no other font specified, the builder will also apply this font to all characters that it inserts.
self.assertEqual("Calibri", builder.font.name)

# Specify a font to use for all characters outside of the ASCII range.
# Ideally, this font should have a glyph for each required non-ASCII character code.
builder.font.name_other = "Courier New"

# Insert a run with one word consisting of ASCII characters, and one word with all characters outside that range.
# Each character will be displayed using either of the fonts, depending on.
builder.writeln("Hello, Привет")

doc.save(ARTIFACTS_DIR + "Font.name_ascii.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

