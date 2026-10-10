---
title: FieldSeq.reset_number property
linktitle: reset_number property
articleTitle: reset_number property
second_title: Aspose.Words for Python
description: "FieldSeq.reset_number property. Gets or sets an integer number to reset the sequence number to"
type: docs
weight: 50
url: /sv/python-net/aspose.words.fields/fieldseq/reset_number/
---

## FieldSeq.reset_number property

Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent.


```python
@property
def reset_number(self) -> str:
    ...

@reset_number.setter
def reset_number(self, value: str):
    ...

```

### Examples

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Infoga ett SEQ‑fält som kommer att visa det aktuella räknarvärdet för "MySequence",
# efter att ha använt egenskapen "ResetNumber" för att sätta den till 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# Visa nästa nummer i denna sekvens med ett annat SEQ‑fält.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# Infoga en rubrik på nivå 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# Infoga ett annat SEQ‑fält från samma sekvens och konfigurera det att återställa räknaren till 1 vid varje rubrik.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# Ovanstående rubrik är en rubrik på nivå 1, så räknaren för denna sekvens återställs till 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# Gå till nästa nummer i den här sekvensen.
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

