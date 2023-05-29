---
title: FieldToc.prefixed_sequence_identifier property
linktitle: prefixed_sequence_identifier property
articleTitle: prefixed_sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.prefixed_sequence_identifier property. Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number."
type: docs
weight: 120
url: /python-net/aspose.words.fields/fieldtoc/prefixed_sequence_identifier/
---

## FieldToc.prefixed_sequence_identifier property

Gets or sets the identifier of a sequence for which a prefix should be added to the entry's page number.


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
field_toc.table_of_figures_label = "MySequence"

# We can name another SEQ field sequence in the "prefixed_sequence_identifier" property.
# SEQ fields from this prefix sequence will not create TOC entries.
# Every TOC entry created from a main sequence SEQ field will now also display the count that
# the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
field_toc.prefixed_sequence_identifier = "PrefixSequence"

# Each TOC entry will display the prefix sequence count immediately to the left
# of the page number that the main sequence SEQ field appears on.
# We can specify a custom separator that will appear between these two numbers.
field_toc.sequence_separator = ">"

self.assertEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", field_toc.get_field_code())

builder.insert_break(aw.BreakType.PAGE_BREAK)

# There are two ways of using SEQ fields to populate this TOC.
# 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
# This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
# Since this field does not belong to the main sequence identified
# by the "table_of_figures_label" property of the TOC, it will not appear as an entry.
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "PrefixSequence"
builder.insert_paragraph()

self.assertEqual(" SEQ  PrefixSequence", field_seq.get_field_code())

# 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
# This SEQ field will create an entry in the TOC.
# The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
# This entry will also display the count that the prefix sequence is currently at,
# separated from the page number by the value in the TOC's "seqence_separator" property.
# The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
# and the separator is ">", so entry will display "1>2".
builder.write("First TOC entry, MySequence #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"

self.assertEqual(" SEQ  MySequence", field_seq.get_field_code())

# Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
# The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
# so the TOC entry will display "2>3" at its page count.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "PrefixSequence"
builder.insert_paragraph()
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
builder.write("Second TOC entry, MySequence #")
field_seq.sequence_identifier = "MySequence"

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.toc_seq_prefix.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

