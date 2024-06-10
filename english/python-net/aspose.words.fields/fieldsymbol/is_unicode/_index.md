---
title: FieldSymbol.is_unicode property
linktitle: is_unicode property
articleTitle: is_unicode property
second_title: Aspose.Words for Python
description: "FieldSymbol.is_unicode property. Gets or sets whether the character code is interpreted as the value of a Unicode character."
type: docs
weight: 80
url: /python-net/aspose.words.fields/fieldsymbol/is_unicode/
---

## FieldSymbol.is_unicode property

Gets or sets whether the character code is interpreted as the value of a Unicode character.


```python
@property
def is_unicode(self) -> bool:
    ...

@is_unicode.setter
def is_unicode(self, value: bool):
    ...

```

### Examples

Shows how to use the SYMBOL field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Below are three ways to use a SYMBOL field to display a single character.
# 1 -  Add a SYMBOL field which displays the © (Copyright) symbol, specified by an ANSI character code:
field = builder.insert_field(aw.fields.FieldType.FIELD_SYMBOL, True).as_field_symbol()
# The ANSI character code "U+00A9", or "169" in integer form, is reserved for the copyright symbol.
field.character_code = '169'
field.is_ansi = True
self.assertEqual(' SYMBOL  169 \\a', field.get_field_code())
builder.writeln(' Line 1')
# 2 -  Add a SYMBOL field which displays the ∞ (Infinity) symbol, and modify its appearance:
field = builder.insert_field(aw.fields.FieldType.FIELD_SYMBOL, True).as_field_symbol()
# In Unicode, the infinity symbol occupies the "221E" code.
field.character_code = str(8734)
field.is_unicode = True
# Change the font of our symbol after using the Windows Character Map
# to ensure that the font can represent that symbol.
field.font_name = 'Calibri'
field.font_size = '24'
# We can set this flag for tall symbols to make them not push down the rest of the text on their line.
field.dont_affects_line_spacing = True
self.assertEqual(' SYMBOL  8734 \\u \\f Calibri \\s 24 \\h', field.get_field_code())
builder.writeln('Line 2')
# 3 -  Add a SYMBOL field which displays the あ character,
# with a font that supports Shift-JIS (Windows-932) codepage:
field = builder.insert_field(aw.fields.FieldType.FIELD_SYMBOL, True).as_field_symbol()
field.font_name = 'MS Gothic'
field.character_code = str(33440)
field.is_shift_jis = True
self.assertEqual(' SYMBOL  33440 \\f "MS Gothic" \\j', field.get_field_code())
builder.write('Line 3')
doc.save(ARTIFACTS_DIR + 'Field.field_symbol.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSymbol](../)

