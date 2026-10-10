---
title: FieldIndex.cross_reference_separator property
linktitle: cross_reference_separator property
articleTitle: cross_reference_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.cross_reference_separator property. Gets or sets the character sequence that is used to separate cross references and other entries."
type: docs
weight: 30
url: /sv/python-net/aspose.words.fields/fieldindex/cross_reference_separator/
---

## FieldIndex.cross_reference_separator property

Gets or sets the character sequence that is used to separate cross references and other entries.


```python
@property
def cross_reference_separator(self) -> str:
    ...

@cross_reference_separator.setter
def cross_reference_separator(self, value: str):
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
* class [FieldIndex](../)

