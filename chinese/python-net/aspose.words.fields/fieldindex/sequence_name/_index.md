---
title: FieldIndex.sequence_name property
linktitle: sequence_name property
articleTitle: sequence_name property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_name property. Gets or sets the name of a sequence whose number is included with the page number."
type: docs
weight: 150
url: /zh/python-net/aspose.words.fields/fieldindex/sequence_name/
---

## FieldIndex.sequence_name property

Gets or sets the name of a sequence whose number is included with the page number.


```python
@property
def sequence_name(self) -> str:
    ...

@sequence_name.setter
def sequence_name(self, value: str):
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# 如果 XE 字段在其 \"Text\" 属性中的值相同，
# INDEX 字段会将它们合并为一个条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# 在 SequenceName 属性中，为 SEQ 字段序列命名。此 INDEX 字段的每个条目现在还将显示
# 在创建此条目的 XE 字段位置处的序列计数所在的数字。
index.sequence_name = 'MySequence'
# 设置文本环绕序列和页码，以向用户解释它们的含义。
# 使用此配置创建的条目将在其页码处显示类似 "MySequence at 1 on page 1" 的内容。
# PageNumberSeparator 和 SequenceSeparator 的长度不能超过 15 个字符。
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# SEQ 域显示一个在每个 SEQ 域递增的计数。
# 这些域还为每个唯一命名的序列维护单独的计数
# 由 SEQ 域的 "SequenceIdentifier" 属性标识。
# 插入一个 SEQ 字段，将 "MySequence" 序列移动到 1。
# 此字段与普通文档文本没有区别。它不会出现在 INDEX 字段的目录中。
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# 插入一个 XE 字段，它将在 INDEX 字段中创建一个条目。
# 由于 "MySequence" 位于 1 且此 XE 字段在第 2 页，加上我们上面定义的自定义分隔符，
# 此字段的 INDEX 条目将在左侧显示 "Cat"，右侧显示 "MySequence at 1 on page 2"。
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# 插入分页符并使用 SEQ 字段将 "MySequence" 推进到 3。
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# 插入一个 XE 字段，其 Text 属性与上面的相同。
# INDEX 条目将把具有匹配 \"Text\" 属性值的 XE 字段分组
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
# 由于我们在第 2 页且 "MySequence" 为 3，", 3 on page 3" 将追加到上述同一 INDEX 条目中。
# 该 INDEX 条目的页码部分现在将显示 "MySequence at 1 on page 2, 3 on page 3"。
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# 插入一个具有全新且唯一 Text 属性值的 XE 字段。
# 这将添加一个新条目，MySequence at 3 on page 4。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

