---
title: FieldIndex.has_sequence_name property
linktitle: has_sequence_name property
articleTitle: has_sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.has_sequence_name property. Gets a value indicating whether a sequence should be used while the field's result building."
type: docs
weight: 60
url: /sv/python-net/aspose.words.fields/fieldindex/has_sequence_name/
---

## FieldIndex.has_sequence_name property

Gets a value indicating whether a sequence should be used while the field's result building.


```python
@property
def has_sequence_name(self) -> bool:
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# Om XE-fälten har samma värde i deras "Text"-egenskap,
# kommer INDEX-fältet att gruppera dem till en post.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# I egenskapen SequenceName, namnge en SEQ-fältsekvens. Varje post i detta INDEX-fält kommer nu också att visa
# numret som sekvensräkningen är på vid XE-fältets plats som skapade denna post.
index.sequence_name = 'MySequence'
# Ange text som kommer runt sekvensen och sidnumren för att förklara deras betydelse för användaren.
# En post som skapats med denna konfiguration kommer att visa något i stil med "MySequence at 1 on page 1" vid dess sidnummer.
# PageNumberSeparator och SequenceSeparator får inte vara längre än 15 tecken.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# SEQ-fält visar ett räknare som ökas vid varje SEQ-fält.
# Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
# identifierad av SEQ-fältets egenskap "SequenceIdentifier".
# Infoga ett SEQ-fält som flyttar "MySequence"-sekvensen till 1.
# Detta fält är inte annorlunda än normal dokumenttext. Det kommer inte att visas i ett INDEX-fälts innehållsförteckning.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# Infoga ett XE-fält som kommer att skapa en post i INDEX-fältet.
# Eftersom "MySequence" är på 1 och detta XE-fält är på sida 2, tillsammans med de anpassade avgränsare vi definierade ovan,
# kommer detta fälts INDEX-post att visa "Cat" på vänster sida, och "MySequence at 1 on page 2" på höger sida.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# Infoga ett sidbryt och använd SEQ-fält för att avancera "MySequence" till 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# Infoga ett XE-fält med samma Text-egenskap som den ovan.
# INDEX-posten kommer att gruppera XE-fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
# Eftersom vi är på sida 2 med "MySequence" på 3, ", 3 på sida 3" kommer att läggas till i samma INDEX-post som ovan.
# Sidnummerdelen av den INDEX-posten kommer nu att visa "MySequence at 1 on page 2, 3 on page 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# Infoga ett XE-fält med ett nytt och unikt Text-egenskapsvärde.
# Detta kommer att lägga till en ny post, med MySequence på 3 på sida 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

