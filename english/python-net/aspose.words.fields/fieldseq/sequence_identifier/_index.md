---
title: FieldSeq.sequence_identifier property
linktitle: sequence_identifier property
articleTitle: sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldSeq.sequence_identifier property. Gets or sets the name assigned to the series of items that are to be numbered."
type: docs
weight: 60
url: /python-net/aspose.words.fields/fieldseq/sequence_identifier/
---

## FieldSeq.sequence_identifier property

Gets or sets the name assigned to the series of items that are to be numbered.


```python
@property
def sequence_identifier(self) -> str:
    ...

@sequence_identifier.setter
def sequence_identifier(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# A TOC field can create an entry in its table of contents for each SEQ field found in the document.
# Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()
# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Use the "table_of_figures_label" property to name a main sequence for the TOC.
# Now, this TOC will only create entries out of SEQ fields with their "sequence_identifier" set to "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# We can name another SEQ field sequence in the "prefixed_sequence_identifier" property.
# SEQ fields from this prefix sequence will not create TOC entries.
# Every TOC entry created from a main sequence SEQ field will now also display the count that
# the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# Each TOC entry will display the prefix sequence count immediately to the left
# of the page number that the main sequence SEQ field appears on.
# We can specify a custom separator that will appear between these two numbers.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# There are two ways of using SEQ fields to populate this TOC.
# 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
# This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
# Since this field does not belong to the main sequence identified
# by the "table_of_figures_label" property of the TOC, it will not appear as an entry.
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
# This SEQ field will create an entry in the TOC.
# The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
# This entry will also display the count that the prefix sequence is currently at,
# separated from the page number by the value in the TOC's "seqence_separator" property.
# The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
# and the separator is ">", so entry will display "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
# The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
# so the TOC entry will display "2>3" at its page count.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.toc_seq_prefix.docx')
```

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field that will display the current count value of "MySequence",
# after using the "reset_number" property to set it to 100.
builder.write('#')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Display the next number in this sequence with another SEQ field.
builder.write(', #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Insert a level 1 heading.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
builder.write('\n#')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# The above heading is a level 1 heading, so the count for this sequence is reset to 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Move to the next number of this sequence.
builder.write(', #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.toc_seq_numbering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

