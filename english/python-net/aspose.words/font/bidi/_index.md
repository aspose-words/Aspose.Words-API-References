---
title: Font.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "Font.bidi property. Specifies whether the contents of this run shall have right-to-left characteristics."
type: docs
weight: 30
url: /python-net/aspose.words/font/bidi/
---

## Font.bidi property

Specifies whether the contents of this run shall have right-to-left characteristics.

This property, when on, shall not be used with strongly left-to-right text. Any behavior under that condition is unspecified.
This property, when off, shall not be used with strong right-to-left text. Any behavior under that condition is unspecified.

When the contents of this run are displayed, all characters shall be treated as complex script characters for formatting
purposes. This means that [Font.bold_bi](../bold_bi/), [Font.italic_bi](../italic_bi/), [Font.size_bi](../size_bi/) and a corresponding font name
will be used when rendering this run.

Also, when the contents of this run are displayed, this property acts as a right-to-left override for characters
which are classified as "weak types" and "neutral types".




### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Define a set of font settings for left-to-right text.
builder.font.name = "Courier New"
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033 # en-US

# Define another set of font settings for right-to-left text.
builder.font.name_bi = "Andalus"
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096 # ar-AR

# We can use the "bidi" flag to indicate whether the text we are about to add
# with the document builder is right-to-left. When we add text with this flag set to True,
# it will be formatted using the right-to-left set of font settings.
builder.font.bidi = True
builder.write("مرحبًا")

# Set the flag to "False", and then add left-to-right text.
# The document builder will format these using the left-to-right set of font settings.
builder.font.bidi = False
builder.write(" Hello world!")

doc.save(ARTIFACTS_DIR + "Font.bidi.docx")
```

### See Also

* module [aspose.words](../../)
* class [Font](../)

