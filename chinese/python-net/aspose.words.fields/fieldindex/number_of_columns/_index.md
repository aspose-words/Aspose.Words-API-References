---
title: FieldIndex.number_of_columns property
linktitle: number_of_columns property
articleTitle: number_of_columns property
second_title: Aspose.Words for Python
description: "FieldIndex.number_of_columns property. Gets or sets the number of columns per page used when building the index."
type: docs
weight: 100
url: /zh/python-net/aspose.words.fields/fieldindex/number_of_columns/
---

## FieldIndex.number_of_columns property

Gets or sets the number of columns per page used when building the index.


```python
@property
def number_of_columns(self) -> str:
    ...

@number_of_columns.setter
def number_of_columns(self, value: str):
    ...

```

### Examples

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# 如果 XE 字段在其 \"Text\" 属性中的值相同，
# INDEX 字段会将它们合并为一个条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# 将此属性的值设置为 "A" 将把所有条目按首字母分组，
# 并在每个组上方以大写形式放置该字母。
index.heading = 'A'
# 将 INDEX 字段创建的表格设置为跨越 2 列。
index.number_of_columns = '2'
# 将首字母超出 "a-c" 范围的任何条目设置为省略。
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# 接下来的两个 XE 字段将显示在 "A" 标题下，
# 并且它们各自的文本样式也会应用于页面编号。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# 接下来的两个 XE 字段将在 INDEX 字段的目录中分别位于 "B" 和 "C" 标题下。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# INDEX 字段按字母顺序对所有条目进行排序，因此此条目将与另外两个一起显示在 "A" 下。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# 此条目不会出现，因为它以字母 "D" 开头，
# 这超出了 INDEX 字段的 LetterRange 属性定义的 "a-c" 字符范围。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

