---
title: FieldSymbol class
linktitle: FieldSymbol class
articleTitle: FieldSymbol class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSymbol class. Implements a SYMBOL field"
type: docs
weight: 1000
url: /python-net/aspose.words.fields/fieldsymbol/
---

## FieldSymbol class

Implements a SYMBOL field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the character whose code point value is specified in decimal or hexadecimal.


**Inheritance:** [FieldSymbol](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSymbol()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [character_code](./character_code/) | Gets or sets the character's code point value in decimal or hexadecimal. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [dont_affects_line_spacing](./dont_affects_line_spacing/) | Gets or sets whether the character retrieved by the field affects the line spacing of the paragraph. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [font_name](./font_name/) | Gets or sets the name of the font of the character retrieved by the field. |
| [font_size](./font_size/) | Gets or sets the size in points of the font of the character retrieved by the field. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_ansi](./is_ansi/) | Gets or sets whether the character code is interpreted as the value of an ANSI character. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [is_shift_jis](./is_shift_jis/) | Gets or sets whether the character code is interpreted as the value of a SHIFT-JIS character. |
| [is_unicode](./is_unicode/) | Gets or sets whether the character code is interpreted as the value of a Unicode character. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

