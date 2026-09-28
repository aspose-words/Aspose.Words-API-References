---
title: FieldToc.entry_identifier property
linktitle: entry_identifier property
articleTitle: entry_identifier property
second_title: Aspose.Words for Python
description: "FieldToc.entry_identifier property. Gets or sets a string that should match type identifiers of TC fields being included."
type: docs
weight: 50
url: /zh/python-net/aspose.words.fields/fieldtoc/entry_identifier/
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
# 插入 TOC 字段，它会将所有 TC 字段编入目录。
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# 配置字段仅获取类型为 \"A\" 的 TC 条目，且条目级别在 1 到 3 之间。
field_toc.entry_identifier = 'A'
field_toc.entry_level_range = '1-3'
self.assertEqual(' TOC  \\f A \\l 1-3', field_toc.get_field_code())
# 这两个条目将出现在目录中。
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.insert_toc_entry(builder, 'TC field 1', 'A', '1')
self.insert_toc_entry(builder, 'TC field 2', 'A', '2')
self.assertEqual(' TC  "TC field 1" \\n \\f A \\l 1', doc.range.fields[1].get_field_code())
# 此条目将从目录中省略，因为它的类型不同于 \"A\"。
self.insert_toc_entry(builder, 'TC field 3', 'B', '1')
# 此条目将从目录中省略，因为它的条目级别超出 1-3 范围。
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

