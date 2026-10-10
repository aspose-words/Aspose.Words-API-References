---
title: FieldIndex.page_number_separator property
linktitle: page_number_separator property
articleTitle: page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_number_separator property. Gets or sets the character sequence that is used to separate an index entry and its page number."
type: docs
weight: 120
url: /sv/python-net/aspose.words.fields/fieldindex/page_number_separator/
---

## FieldIndex.page_number_separator property

Gets or sets the character sequence that is used to separate an index entry and its page number.


```python
@property
def page_number_separator(self) -> str:
    ...

@page_number_separator.setter
def page_number_separator(self, value: str):
    ...

```

### Examples

Shows how to edit the page number separator in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# INDEX-posten kommer att gruppera XE-fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Om vårt INDEX-fält har en post för en grupp av XE-fält,
# kommer denna post att visa numret på varje sida som innehåller ett XE-fält som tillhör denna grupp.
# Vi kan ställa in anpassade avgränsare för att anpassa utseendet på dessa sidnummer.
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# Efter att vi har infogat dessa XE-fält kommer INDEX-fältet att visa "Första posten, på sida(s) 2 & 3 & 4".
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
self.assertEqual(' XE  "First entry"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'First entry'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageNumberList.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

