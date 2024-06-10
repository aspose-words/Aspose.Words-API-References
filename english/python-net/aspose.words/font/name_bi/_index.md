---
title: Font.name_bi property
linktitle: name_bi property
articleTitle: name_bi property
second_title: Aspose.Words for Python
description: "Font.name_bi property. Returns or sets the name of the font in a right-to-left language document."
type: docs
weight: 250
url: /python-net/aspose.words/font/name_bi/
---

## Font.name_bi property

Returns or sets the name of the font in a right-to-left language document.


```python
@property
def name_bi(self) -> str:
    ...

@name_bi.setter
def name_bi(self, value: str):
    ...

```

### Examples

Shows how to define separate sets of font settings for right-to-left, and right-to-left text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Define a set of font settings for left-to-right text.
builder.font.name = 'Courier New'
builder.font.size = 16
builder.font.italic = False
builder.font.bold = False
builder.font.locale_id = 1033  # en-US
# Define another set of font settings for right-to-left text.
builder.font.name_bi = 'Andalus'
builder.font.size_bi = 24
builder.font.italic_bi = True
builder.font.bold_bi = True
builder.font.locale_id_bi = 4096  # ar-AR
# We can use the "bidi" flag to indicate whether the text we are about to add
# with the document builder is right-to-left. When we add text with this flag set to True,
# it will be formatted using the right-to-left set of font settings.
builder.font.bidi = True
builder.write('مرحبًا')
# Set the flag to "False", and then add left-to-right text.
# The document builder will format these using the left-to-right set of font settings.
builder.font.bidi = False
builder.write(' Hello world!')
doc.save(ARTIFACTS_DIR + 'Font.bidi.docx')
```

### See Also

* module [aspose.words](../../)
* class [Font](../)
* property [Font.name](../name/)

