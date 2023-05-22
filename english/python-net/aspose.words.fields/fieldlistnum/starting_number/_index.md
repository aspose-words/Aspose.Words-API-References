---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldlistnum/starting_number/
---

## FieldListNum.starting_number property

Gets or sets the starting value for this field.


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

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

