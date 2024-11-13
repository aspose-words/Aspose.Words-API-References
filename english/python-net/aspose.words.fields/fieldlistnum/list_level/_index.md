---
title: FieldListNum.list_level property
linktitle: list_level property
articleTitle: list_level property
second_title: Aspose.Words for Python
description: "FieldListNum.list_level property. Gets or sets the level in the list, overriding the default behavior of the field."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldlistnum/list_level/
---

## FieldListNum.list_level property

Gets or sets the level in the list, overriding the default behavior of the field.


```python
@property
def list_level(self) -> str:
    ...

@list_level.setter
def list_level(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# LISTNUM fields display a number that increments at each LISTNUM field.
# These fields also have a variety of options that allow us to use them to emulate numbered lists.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Lists start counting at 1 by default, but we can set this number to a different value, such as 0.
# This field will display "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# LISTNUM fields maintain separate counts for each list level.
# Inserting a LISTNUM field in the same paragraph as another LISTNUM field
# increases the list level instead of the count.
# The next field will continue the count we started above and display a value of "1" at list level 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# This field will start a count at list level 2. It will display a value of "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# This field will start a count at list level 3. It will display a value of "1".
# Different list levels have different formatting,
# so these fields combined will display a value of "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# The next LISTNUM field that we insert will continue the count at the list level
# that the previous LISTNUM field was on.
# We can use the "ListLevel" property to jump to a different list level.
# If this LISTNUM field stayed on list level 3, it would display "ii)",
# but, since we have moved it to list level 2, it carries on the count at that level and displays "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# We can set the ListName property to get the field to emulate a different AUTONUM field type.
# "NumberDefault" emulates AUTONUM, "OutlineDefault" emulates AUTONUMOUT,
# and "LegalDefault" emulates AUTONUMLGL fields.
# The "OutlineDefault" list name with 1 as the starting number will result in displaying "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# The ListName does not carry over from the previous field, so we will need to set it for each new field.
# This field continues the count with the different list name and displays "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

