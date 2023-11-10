---
title: FieldSeq.insert_next_number property
linktitle: insert_next_number property
articleTitle: insert_next_number property
second_title: Aspose.Words for Python
description: "FieldSeq.insert_next_number property. Gets or sets whether to insert the next sequence number for the specified item."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldseq/insert_next_number/
---

## FieldSeq.insert_next_number property

Gets or sets whether to insert the next sequence number for the specified item.


```python
@property
def insert_next_number(self) -> bool:
    ...

@insert_next_number.setter
def insert_next_number(self, value: bool):
    ...

```

### Examples

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field that will display the current count value of "MySequence",
# after using the "reset_number" property to set it to 100.
builder.write("#")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.reset_number = "100"
field_seq.update()

self.assertEqual(" SEQ  MySequence \\r 100", field_seq.get_field_code())
self.assertEqual("100", field_seq.result)

# Display the next number in this sequence with another SEQ field.
builder.write(", #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.update()

self.assertEqual("101", field_seq.result)

# Insert a level 1 heading.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name("Heading 1")
builder.writeln("This level 1 heading will reset MySequence to 1")
builder.paragraph_format.style = doc.styles.get_by_name("Normal")

# Insert another SEQ field from the same sequence and configure it to reset the count at every heading with 1.
builder.write("\n#")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.reset_heading_level = "1"
field_seq.update()

# The above heading is a level 1 heading, so the count for this sequence is reset to 1.
self.assertEqual(" SEQ  MySequence \\s 1", field_seq.get_field_code())
self.assertEqual("1", field_seq.result)

# Move to the next number of this sequence.
builder.write(", #")
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = "MySequence"
field_seq.insert_next_number = True
field_seq.update()

self.assertEqual(" SEQ  MySequence \\n", field_seq.get_field_code())
self.assertEqual("2", field_seq.result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.toc_seq_numbering.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

