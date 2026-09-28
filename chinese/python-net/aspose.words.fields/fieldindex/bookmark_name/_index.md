---
title: FieldIndex.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldIndex.bookmark_name property. Gets or sets the name of the bookmark that marks the portion of the document used to build the index."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldindex/bookmark_name/
---

## FieldIndex.bookmark_name property

Gets or sets the name of the bookmark that marks the portion of the document used to build the index.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值
# 以及包含 XE 字段的页码在右侧。
# 如果 XE 字段在其 \"Text\" 属性中的值相同，
# INDEX 字段会将它们合并为一个条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# 配置 INDEX 字段仅显示位于范围内的 XE 字段
# 该范围为名为 \"MainBookmark\" 的书签，并且其 \"EntryType\" 属性的值为 \"A\"。
# 对于 INDEX 和 XE 字段，\"EntryType\" 属性仅使用其字符串值的第一个字符。
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# 在新页面上，使用与该值匹配的名称启动书签
# 该值为 INDEX 字段的 \"BookmarkName\" 属性。
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# INDEX 字段会捕获此条目，因为它位于书签内部，
# 且其条目类型也匹配 INDEX 字段的条目类型。
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# 插入一个 XE 字段，由于条目类型不匹配，它不会出现在 INDEX 中。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# 结束书签并随后插入一个 XE 字段。
# 它与 INDEX 字段属于相同类型，但不会出现
# 因为它超出了书签的边界。
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
* class [FieldIndex](../)

