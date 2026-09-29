---
title: FieldIndex.page_range_separator property
linktitle: page_range_separator property
articleTitle: page_range_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_range_separator property. Gets or sets the character sequence that is used to separate the start and end of a page range."
type: docs
weight: 130
url: /sv/python-net/aspose.words.fields/fieldindex/page_range_separator/
---

## FieldIndex.page_range_separator property

Gets or sets the character sequence that is used to separate the start and end of a page range.


```python
@property
def page_range_separator(self) -> str:
    ...

@page_range_separator.setter
def page_range_separator(self, value: str):
    ...

```

### Examples

Shows how to specify a bookmark's spanned pages as a page range for an INDEX field entry.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett INDEX-fält som kommer att visa en post för varje XE-fält som finns i dokumentet.
# Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
# och sidnumret som innehåller XE-fältet på höger sida.
# INDEX‑posten kommer att samla alla XE‑fält med matchande värden i egenskapen "Text"
# till en enda post istället för att skapa en post för varje XE‑fält.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# För INDEX-poster som visar sidintervall kan vi ange en separatorsträng
# som kommer att visas mellan numret på den första sidan och numret på den sista.
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# Om ett XE-fält namnger ett bokmärke med hjälp av egenskapen PageRangeBookmarkName,
# kommer dess INDEX-post att visa intervallet av sidor som bokmärket sträcker sig över.
# istället för numret på sidan som innehåller XE-fältet.
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# Infoga ett bokmärke som börjar på sida 3 och slutar på sida 5.
# INDEX-posten för XE-fältet som refererar till detta bokmärke kommer att visa detta sidintervall.
# I vår tabell kommer INDEX-posten att visa "My entry, on page(s) 3 to 5".
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MyBookmark')
builder.write('Start of MyBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('End of MyBookmark')
builder.end_bookmark('MyBookmark')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.PageRangeBookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

