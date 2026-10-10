---
title: FieldToc.entry_identifier property
linktitle: entry_identifier property
articleTitle: entry_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.entry_identifier property. Gets or sets a string that should match type identifiers of TC fields being included."
type: docs
weight: 50
url: /de/python-net/aspose.words.fields/fieldtoc/entry_identifier/
---

## FieldToc.entry_identifier property

Gets or sets a string that should match type identifiers of TC fields being included.


```python
@property
def entry_identifier(self) -> str:
    ...

@entry_identifier.setter
def entry_identifier(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein TOC-Feld ein, das alle TC-Felder zu einem Inhaltsverzeichnis zusammenfasst.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# Konfigurieren Sie das Feld so, dass nur TC-Einträge des Typs "A" und ein Eintragslevel zwischen 1 und 3 übernommen werden.
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# Diese beiden Einträge werden im Verzeichnis erscheinen.
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# Dieser Eintrag wird im Verzeichnis ausgelassen, weil er einen anderen Typ als "A" hat.
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# Dieser Eintrag wird im Verzeichnis ausgelassen, weil sein Eintragslevel außerhalb des Bereichs 1‑3 liegt.
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

