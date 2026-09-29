---
title: FieldXE.page_number_replacement property
linktitle: page_number_replacement property
articleTitle: page_number_replacement property
second_title: Aspose.Words for Python
description: "FieldXE.page_number_replacement property. Gets or sets text used in place of a page number."
type: docs
weight: 50
url: /sv/python-net/aspose.words.fields/fieldxe/page_number_replacement/
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
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# INDEX‑posten kommer att samla alla XE‑fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Vi kan konfigurera ett XE‑fält så att dess INDEX‑post visar en sträng istället för ett sidnummer.
# Först, för poster som ersätter ett sidnummer med en sträng,
# ange en anpassad separator mellan XE‑fältets Text‑egenskapsvärde och strängen.
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# Infoga ett XE‑fält, som skapar en vanlig INDEX‑post som visar detta fälts sidnummer,
# och som inte använder värdet CrossReferenceSeparator.
# Posten för detta XE‑fält kommer att visa "Apple, 2".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# Infoga ett annat XE‑fält på sida 3 och ange ett värde för egenskapen PageNumberReplacement.
# Detta värde kommer att visas istället för numret på den sida som detta fält är på,
# och INDEX‑fältets CrossReferenceSeparator‑värde kommer att visas framför det.
# Posten för detta XE‑fält kommer att visa "Banana, se: Tropisk frukt".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

