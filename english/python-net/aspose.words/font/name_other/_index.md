---
title: Font.name_other property
linktitle: name_other property
articleTitle: name_other property
second_title: Aspose.Words for Python
description: "Font.name_other property. Returns or sets the font used for characters with character codes from 128 through 255."
type: docs
weight: 270
url: /python-net/aspose.words/font/name_other/
---

## Font.name_other property

Returns or sets the font used for characters with character codes from 128 through 255.


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

