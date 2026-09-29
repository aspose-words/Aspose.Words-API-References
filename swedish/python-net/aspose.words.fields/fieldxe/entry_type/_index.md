---
title: FieldXE.entry_type property
linktitle: entry_type property
articleTitle: entry_type property
second_title: Aspose.Words for Python
description: "FieldXE.entry_type property. Gets or sets an index entry type."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldxe/entry_type/
---

## FieldXE.entry_type property

Gets or sets an index entry type.


```python
@property
def entry_type(self) -> str:
    ...

@entry_type.setter
def entry_type(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida
# och sidan som innehåller XE-fältet på höger sida.
# Om XE-fälten har samma värde i deras "Text"-egenskap,
# kommer INDEX-fältet att gruppera dem till en post.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Konfigurera INDEX-fältet så att det endast visar XE-fält som ligger inom gränserna
# för ett bokmärke med namnet "MainBookmark" och vars "EntryType"-egenskaper har värdet "A".
# För både INDEX- och XE-fält använder "EntryType"-egenskapen endast det första tecknet i dess strängvärde.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# På en ny sida, starta bokmärket med ett namn som matchar värdet
# för INDEX-fältets "BookmarkName"-egenskap.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# INDEX-fältet kommer att plocka upp den här posten eftersom den är inne i bokmärket,
# och dess posttyp matchar också INDEX-fältets posttyp.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Infoga ett XE-fält som inte kommer att visas i INDEX eftersom posttyperna inte matchar.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Avsluta bokmärket och infoga ett XE-fält därefter.
# Det är av samma typ som INDEX-fältet, men kommer inte att visas
# eftersom den ligger utanför bokmärkets gränser.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldXE](../)

