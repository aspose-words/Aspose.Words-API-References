---
title: FieldListNum class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the LISTNUM field."
type: docs
weight: 660
url: /python-net/aspose.words.fields/fieldlistnum/
---

## FieldListNum class

Implements the LISTNUM field.


**Inheritance:** [FieldListNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldListNum()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [has_list_name](./has_list_name/) | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [list_level](./list_level/) | Gets or sets the level in the list, overriding the default behavior of the field. |
| [list_name](./list_name/) | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [starting_number](./starting_number/) | Gets or sets the starting value for this field. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# LISTNUM fields display a number that increments at each LISTNUM field.
# These fields also have a variety of options that allow us to use them to emulate numbered lists.
field = builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True).as_field_list_num()

# Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
# This field will display "0)".
field.starting_number = "0"
builder.writeln("Paragraph 1")

self.assertEqual(" LISTNUM  \\s 0", field.get_field_code())

# LISTNUM fields maintain separate counts for each list level.
# Inserting a LISTNUM field in the same paragraph as another LISTNUM field
# increases the list level instead of the count.
# The next field will continue the count we started above and display a value of "1" at list level 1.
builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True)

# This field will start a count at list level 2. It will display a value of "1".
builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True)

# This field will start a count at list level 3. It will display a value of "1".
# Different list levels have different formatting,
# so these fields combined will display a value of "1)a)i)".
builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True)
builder.writeln("Paragraph 2")

# The next LISTNUM field that we insert will continue the count at the list level
# that the previous LISTNUM field was on.
# We can use the "list_level" property to jump to a different list level.
# If this LISTNUM field stayed on list level 3, it would display "ii)",
# but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True).as_field_list_num()
field.list_level = "2"
builder.writeln("Paragraph 3")

self.assertEqual(" LISTNUM  \\l 2", field.get_field_code())

# We can set the list_name property to get the field to emulate a different AUTONUM field type.
# "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
# and "LegalDefault" emulates AUTONUMLGL fields.
# The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True).as_field_list_num()
field.starting_number = "1"
field.list_name = "OutlineDefault"
builder.writeln("Paragraph 4")

self.assertTrue(field.has_list_name)
self.assertEqual(" LISTNUM  OutlineDefault \\s 1", field.get_field_code())

# The list_name does not carry over from the previous field, so we will need to set it for each new field.
# This field continues the count with the different list name and displays "II.".
field = builder.insert_field(aw.fields.FieldType.FIELD_LIST_NUM, True).as_field_list_num()
field.list_name = "OutlineDefault"
builder.writeln("Paragraph 5")

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_list_num.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

