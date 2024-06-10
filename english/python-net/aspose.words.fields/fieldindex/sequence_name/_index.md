---
title: FieldIndex.sequence_name property
linktitle: sequence_name property
articleTitle: sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_name property. Gets or sets the name of a sequence whose number is included with the page number."
type: docs
weight: 150
url: /python-net/aspose.words.fields/fieldindex/sequence_name/
---

## FieldIndex.sequence_name property

Gets or sets the name of a sequence whose number is included with the page number.


```python
@property
def sequence_name(self) -> str:
    ...

@sequence_name.setter
def sequence_name(self, value: str):
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Create an INDEX field which will display an entry for each XE field found in the document.
# Each entry will display the XE field's Text property value on the left side,
# and the number of the page that contains the XE field on the right.
# If the XE fields have the same value in their "text" property,
# the INDEX field will group them into one entry.
index = builder.insert_field(aw.fields.FieldType.FIELD_INDEX, True).as_field_index()
# In the sequence_name property, name a SEQ field sequence. Each entry of this INDEX field will now also display
# the number that the sequence count is on at the XE field location that created this entry.
index.sequence_name = 'MySequence'
# Set text that will around the sequence and page numbers to explain their meaning to the user.
# An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
# "page_number_separator" and "sequence_separator" cannot be longer than 15 characters.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field which moves the "MySequence" sequence to 1.
# This field no different from normal document text. It will not appear on an INDEX field's table of contents.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Insert an XE field which will create an entry in the INDEX field.
# Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
# this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Insert a page break and use SEQ fields to advance "MySequence" to 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Insert an XE field with the same "text" property as the one above.
# The INDEX entry will group XE fields with matching values in the "text" property
# into one entry as opposed to making an entry for each XE field.
# Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
# The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = 'Cat'
# Insert an XE field with a new and unique "text" property value.
# This will add a new entry, with MySequence at 3 on page 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(aw.fields.FieldType.FIELD_INDEX_ENTRY, True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_index_sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

