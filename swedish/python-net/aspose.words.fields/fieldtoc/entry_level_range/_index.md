---
title: FieldToc.entry_level_range property
linktitle: entry_level_range property
articleTitle: entry_level_range property
second_title: Aspose.Words for Python
description: "FieldToc.entry_level_range property. Gets or sets a range of levels of the table of contents entries to be included."
type: docs
weight: 60
url: /sv/python-net/aspose.words.fields/fieldtoc/entry_level_range/
---

## FieldToc.entry_level_range property

Gets or sets a range of levels of the table of contents entries to be included.


```python
@property
def entry_level_range(self) -> str:
    ...

@entry_level_range.setter
def entry_level_range(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Infoga ett TOC-fält, som kommer att samla alla TC-fält i en innehållsförteckning.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfigurera fältet så att det bara plockar upp TC-poster av typen "A" och med postnivå mellan 1 och 3.
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# Dessa två poster kommer att visas i tabellen.
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# Denna post kommer att uteslutas från tabellen eftersom den har en annan typ än "A".
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# Denna post kommer att uteslutas från tabellen eftersom den har en postnivå utanför intervallet 1-3.
self.insert_toc_entry(builder, 'TC field 4', 'A', '5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TC.docx')
```

Shows how to insert a TOC field, and filter which TC fields end up as entries (InsertTocEntry).

```python
def insert_toc_entry(self, builder, text, type_identifier, entry_level):
    field_tc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC_ENTRY, update_field=True).as_field_tc()
    field_tc.omit_page_number = True
    field_tc.text = text
    field_tc.type_identifier = type_identifier
    field_tc.entry_level = entry_level
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

