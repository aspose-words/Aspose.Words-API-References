---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldxe/page_number_replacement/
---

## FieldXE.page_number_replacement property

Gets or sets text used in place of a page number.


```python
@property
def page_number_replacement(self) -> str:
    ...

@page_number_replacement.setter
def page_number_replacement(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's "text" property value on the left side,
# and the number of the page that contains the XE field on the right.
# The INDEX entry will collect all XE fields with matching values in the "text" property
# into one entry as opposed to making an entry for each XE field.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()
# We can configure an XE field to get its INDEX entry to display a string instead of a page number.
# First, for entries that substitute a page number with a string,
# specify a custom separator between the XE field's "text" property value and the string.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Insert an XE field, which creates a regular INDEX entry which displays this field's page number,
# and does not invoke the CrossReferenceSeparator value.
# The entry for this XE field will display "Apple, 2".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Insert another XE field on page 3 and set a value for the "page_number_replacement" property.
# This value will show up instead of the number of the page that this field is on,
# and the INDEX field's CrossReferenceSeparator value will appear in front of it.
# The entry for this XE field will display "Banana, see: Tropical fruit".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_index_cross_reference_separator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

