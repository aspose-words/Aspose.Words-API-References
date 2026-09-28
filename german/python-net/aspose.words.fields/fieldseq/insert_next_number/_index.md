---
title: FieldSeq.insert_next_number property
linktitle: insert_next_number property
articleTitle: insert_next_number property
second_title: Aspose.Words for Python
description: "FieldSeq.insert_next_number property. Gets or sets whether to insert the next sequence number for the specified item."
type: docs
weight: 30
url: /de/python-net/aspose.words.fields/fieldseq/insert_next_number/
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
builder = aw.DocumentBuilder(doc=doc)
# SEQ-Felder zeigen eine Zählung an, die bei jedem SEQ-Feld erhöht wird.
# Diese Felder führen außerdem separate Zählungen für jede eindeutig benannte Sequenz.
# identifiziert durch die "SequenceIdentifier"-Eigenschaft des SEQ-Feldes.
# Fügen Sie ein SEQ‑Feld ein, das den aktuellen Zählwert von "MySequence" anzeigt,
# nachdem Sie die "ResetNumber"‑Eigenschaft verwendet haben, um sie auf 100 zu setzen.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Zeigen Sie die nächste Nummer in dieser Sequenz mit einem weiteren SEQ‑Feld an.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Fügen Sie eine Überschrift der Ebene 1 ein.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Fügen Sie ein weiteres SEQ‑Feld aus derselben Sequenz ein und konfigurieren Sie es so, dass die Zählung bei jeder Überschrift mit 1 zurückgesetzt wird.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Die obige Überschrift ist eine Überschrift der Ebene 1, sodass die Zählung für diese Sequenz auf 1 zurückgesetzt wird.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Gehe zur nächsten Nummer dieser Sequenz.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

