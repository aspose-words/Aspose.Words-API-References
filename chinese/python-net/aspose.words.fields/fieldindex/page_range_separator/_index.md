---
title: FieldIndex.page_range_separator property
linktitle: page_range_separator property
articleTitle: page_range_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_range_separator property. Gets or sets the character sequence that is used to separate the start and end of a page range."
type: docs
weight: 130
url: /zh/python-net/aspose.words.fields/fieldindex/page_range_separator/
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
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# 对于显示页码范围的 INDEX 条目，我们可以指定一个分隔符字符串
# 它将出现在第一页的数字和最后一页的数字之间。
index.page_number_separator = ', on page(s) '
index.page_range_separator = ' to '
self.assertEqual(' INDEX  \\e ", on page(s) " \\g " to "', index.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'My entry'
# 如果 XE 字段使用 PageRangeBookmarkName 属性命名书签，
# 它的 INDEX 条目将显示该书签跨越的页码范围
# 而不是包含 XE 字段的页面编号。
index_entry.page_range_bookmark_name = 'MyBookmark'
self.assertEqual(' XE  "My entry" \\r MyBookmark', index_entry.get_field_code())
self.assertEqual('MyBookmark', index_entry.page_range_bookmark_name)
# 插入一个书签，起始于第 3 页，结束于第 5 页。
# 引用此书签的 XE 字段的 INDEX 条目将显示此页码范围。
# 在我们的表格中，INDEX 条目将显示 \"My entry, on page(s) 3 to 5\"。
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

