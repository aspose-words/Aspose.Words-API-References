﻿---
title: FieldAutoNum class
linktitle: FieldAutoNum class
articleTitle: FieldAutoNum class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldAutoNum class. Implements the AUTONUM field"
type: docs
weight: 120
url: /python-net/aspose.words.fields/fieldautonum/
---

## FieldAutoNum class

Implements the AUTONUM field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts an automatic number.


**Inheritance:** [FieldAutoNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAutoNum()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [separator_character](./separator_character/) | Gets or sets the separator character to be used. |
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

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Each AUTONUM field displays the current value of a running count of AUTONUM fields,
# allowing us to automatically number items like a numbered list.
# This field will display a number "1.".
field = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_NUM, True).as_field_auto_num()
builder.writeln("\tParagraph 1.")

self.assertEqual(" AUTONUM ", field.get_field_code())

field = builder.insert_field(aw.fields.FieldType.FIELD_AUTO_NUM, True).as_field_auto_num()
builder.writeln("\tParagraph 2.")

# The separator character, which appears in the field result immediately after the number, is a full stop by default.
# If we leave this property null, our second AUTONUM field will display "2." in the document.
self.assertIsNone(field.separator_character)

# We can set this property to apply the first character of its string as the new separator character.
# In this case, our AUTONUM field will now display "2:".
field.separator_character = ":"

self.assertEqual(" AUTONUM  \\s :", field.get_field_code())

doc.save(ARTIFACTS_DIR + "Field.field_auto_num.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

