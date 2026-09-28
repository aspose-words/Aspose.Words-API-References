---
title: FieldIndex.cross_reference_separator property
linktitle: cross_reference_separator property
articleTitle: cross_reference_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.cross_reference_separator property. Gets or sets the character sequence that is used to separate cross references and other entries."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldindex/cross_reference_separator/
---

## FieldIndex.cross_reference_separator property

Gets or sets the character sequence that is used to separate cross references and other entries.


```python
@property
def cross_reference_separator(self) -> str:
    ...

@cross_reference_separator.setter
def cross_reference_separator(self, value: str):
    ...

```

### Examples

Shows how to define cross references in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# 我们可以配置 XE 字段，使其 INDEX 条目显示字符串而不是页码。
# 首先，对于用字符串替代页码的条目，
# 指定 XE 字段的 Text 属性值与字符串之间的自定义分隔符。
index.cross_reference_separator = ', see: '
self.assertEqual(' INDEX  \\k ", see: "', index.get_field_code())
# 插入 XE 字段，它会创建一个常规的 INDEX 条目，显示该字段的页码，
# 且不调用 CrossReferenceSeparator 值。
# 此 XE 字段的条目将显示 "Apple, 2"。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
self.assertEqual(' XE  Apple', index_entry.get_field_code())
# 在第 3 页插入另一个 XE 字段，并为 PageNumberReplacement 属性设置一个值。
# 此值将显示在该字段所在页的页码位置，
# 并且 INDEX 字段的 CrossReferenceSeparator 值将出现在其前面。
# 此 XE 字段的条目将显示 "Banana, see: Tropical fruit"。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
index_entry.page_number_replacement = 'Tropical fruit'
self.assertEqual(' XE  Banana \\t "Tropical fruit"', index_entry.get_field_code())
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.CrossReferenceSeparator.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

