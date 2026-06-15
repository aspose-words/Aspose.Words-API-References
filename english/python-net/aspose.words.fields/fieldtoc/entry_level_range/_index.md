---
title: FieldToc.entry_level_range property
linktitle: entry_level_range property
articleTitle: entry_level_range property
second_title: Aspose.Words for Python
description: "FieldToc.entry_level_range property. Gets or sets a range of levels of the table of contents entries to be included."
type: docs
weight: 60
url: /python-net/aspose.words.fields/fieldtoc/entry_level_range/
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
# Insert a TOC field, which will compile all TC fields into a table of contents.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# These two entries will appear in the table.
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# This entry will be omitted from the table because it has a different type from "A".
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
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

