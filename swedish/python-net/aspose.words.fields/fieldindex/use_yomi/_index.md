---
title: FieldIndex.use_yomi property
linktitle: use_yomi property
articleTitle: use_yomi property
second_title: Aspose.Words for Python
description: "FieldIndex.use_yomi property. Gets or sets whether to enable the use of yomi text for index entries."
type: docs
weight: 170
url: /sv/python-net/aspose.words.fields/fieldindex/use_yomi/
---

## FieldIndex.use_yomi property

Gets or sets whether to enable the use of yomi text for index entries.


```python
@property
def use_yomi(self) -> bool:
    ...

@use_yomi.setter
def use_yomi(self, value: bool):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# INDEX‑posten kommer att samla alla XE‑fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# INDEX‑tabellen sorterar automatiskt sina poster efter värdena i deras Text‑egenskaper i alfabetisk ordning.
# Ställ in INDEX‑tabellen att sortera poster fonetiskt med Hiragana istället.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# Infoga 4 XE‑fält, som skulle visas som poster i INDEX‑fältets innehållsförteckning.
# Egenskapen "Text" kan innehålla ett ords stavning i Kanji, vars uttal kan vara tvetydigt,
# medan "Yomi"-versionen av ordet exakt visar hur det uttalas med Hiragana.
# Om vi ställer in vårt INDEX-fält för att använda Yomi, kommer det att sortera dessa poster
# efter värdet på deras Yomi-egenskaper, istället för deras Text-värden.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

