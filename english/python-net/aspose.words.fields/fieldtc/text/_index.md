---
title: FieldTC.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldTC.text property. Gets or sets the text of the entry."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldtc/text/
---

## FieldTC.text property

Gets or sets the text of the entry.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```python
def field_toc_entry_identifier():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    # Insert a TOC field, which will compile all TC fields into a table of contents.
    field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()
    # Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
    field_toc.entry_identifier = 'A'
    field_toc.entry_level_range = '1-3'
    self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
    # These two entries will appear in the table.
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    insert_toc_entry(builder, 'TC field 1', 'A', '1')
    insert_toc_entry(builder, 'TC field 2', 'A', '2')
    self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
    # This entry will be omitted from the table because it has a different type from "A".
    insert_toc_entry(builder, 'TC field 3', 'B', '1')
    # This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
    insert_toc_entry(builder, 'TC field 4', 'A', '5')
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + 'Field.tc.docx')

def insert_toc_entry(builder: aw.DocumentBuilder, text: str, type_identifier: str, entry_level: str):
    """Use a document builder to insert a TC field."""
    field_tc = builder.insert_field(aw.fields.FieldType.FIELD_TOC_ENTRY, True).as_field_tc()
    field_tc.omit_page_number = True
    field_tc.text = text
    field_tc.type_identifier = type_identifier
    field_tc.entry_level = entry_level
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldTC](../)

