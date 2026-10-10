---
title: FieldIndex.use_yomi property
linktitle: use_yomi property
articleTitle: use_yomi property
second_title: Aspose.Words for Python
description: "FieldIndex.use_yomi property. Gets or sets whether to enable the use of yomi text for index entries."
type: docs
weight: 170
url: /zh/python-net/aspose.words.fields/fieldindex/use_yomi/
---

## FieldIndex.use_yomi property

Gets or sets whether to enable the use of yomi text for index entries.


```python
@property
def use_yomi(self) -> bool:
    ...

@use_yomi.setter
def use_yomi(self, value: bool):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# INDEX 表会自动按其 Text 属性的值以字母顺序对条目进行排序。
# 将 INDEX 表设置为使用平假名按音序对条目进行排序。
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# 插入 4 个 XE 字段，它们将显示为 INDEX 字段目录中的条目。
# \"Text\"属性可能包含一个单词的汉字拼写，其发音可能含糊，
# 而 \"Yomi\" 版本的单词将使用平假名准确拼写其发音。
# 如果我们将 INDEX 字段设置为使用 Yomi，它将对这些条目进行排序
# 按照它们的 Yomi 属性值，而不是它们的 Text 值。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

