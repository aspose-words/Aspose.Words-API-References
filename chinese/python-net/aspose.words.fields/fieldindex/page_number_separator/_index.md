---
title: FieldIndex.page_number_separator property
linktitle: page_number_separator property
articleTitle: page_number_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.page_number_separator property. Gets or sets the character sequence that is used to separate an index entry and its page number."
type: docs
weight: 120
url: /zh/python-net/aspose.words.fields/fieldindex/page_number_separator/
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
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# INDEX 条目将把具有匹配 \"Text\" 属性值的 XE 字段分组
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# 如果我们的 INDEX 字段有一组 XE 字段的条目，
# 此条目将显示每个包含属于该组的 XE 字段的页面的页码。
# 我们可以设置自定义分隔符来自定义这些页码的外观。
index.page_number_separator = ', on page(s) '
index.page_number_list_separator = ' & '
self.assertEqual(' INDEX  \\e ", on page(s) " \\l " & "', index.get_field_code())
self.assertTrue(index.has_page_number_separator)
# 在插入这些 XE 字段后，INDEX 字段将显示 "First entry, on page(s) 2 & 3 & 4"。
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

