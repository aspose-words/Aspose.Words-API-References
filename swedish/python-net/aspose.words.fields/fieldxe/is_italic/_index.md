---
title: FieldXE.is_italic property
linktitle: is_italic property
articleTitle: is_italic property
second_title: Aspose.Words for Python
description: "FieldXE.is_italic property. Gets or sets whether to apply italic formatting to the entry's page number."
type: docs
weight: 40
url: /sv/python-net/aspose.words.fields/fieldxe/is_italic/
---

## FieldXE.is_italic property

Gets or sets whether to apply italic formatting to the entry's page number.


```python
@property
def is_italic(self) -> bool:
    ...

@is_italic.setter
def is_italic(self, value: bool):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# Om XE-fälten har samma värde i deras "Text"-egenskap,
# kommer INDEX-fältet att gruppera dem till en post.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Om du sätter detta egenskapsvärde till "A" kommer alla poster att grupperas efter deras första bokstav,
# och placera den bokstaven i versaler ovanför varje grupp.
index.heading = 'A'
# Ställ in tabellen som skapas av INDEX-fältet så att den sträcker sig över 2 kolumner.
index.number_of_columns = '2'
# Ställ in att alla poster med startbokstäver utanför teckenuppsättningen "a-c" ska utelämnas.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Dessa två nästa XE-fält kommer att visas under rubriken "A",
# med deras respektive textstilar även tillämpade på deras sidnummer.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Båda de två nästa XE-fälten kommer att vara under rubrikerna "B" och "C" i INDEX-fältets innehållsförteckning.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# INDEX-fält sorterar alla poster alfabetiskt, så den här posten kommer att visas under "A" tillsammans med de andra två.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Denna post kommer inte att visas eftersom den börjar med bokstaven "D",
# vilket ligger utanför teckenuppsättningen "a-c" som INDEX-fältets LetterRange-egenskap definierar.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

