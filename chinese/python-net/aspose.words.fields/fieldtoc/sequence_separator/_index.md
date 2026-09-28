---
title: FieldToc.sequence_separator property
linktitle: sequence_separator property
articleTitle: sequence_separator property
second_title: Aspose.Words for Python
description: "FieldToc.sequence_separator property. Gets or sets the character sequence that is used to separate sequence numbers and page numbers."
type: docs
weight: 150
url: /zh/python-net/aspose.words.fields/fieldtoc/sequence_separator/
---

## FieldToc.sequence_separator property

Gets or sets the character sequence that is used to separate sequence numbers and page numbers.


```python
@property
def sequence_separator(self) -> str:
    ...

@sequence_separator.setter
def sequence_separator(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOC 域可以为文档中找到的每个 SEQ 域在目录中创建一个条目。
# 每个条目包含包含 SEQ 域的段落以及该域所在页的页码。
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# SEQ 域显示一个在每个 SEQ 域递增的计数。
# 这些域还为每个唯一命名的序列维护单独的计数
# 由 SEQ 域的 "SequenceIdentifier" 属性标识。
# 使用 "TableOfFiguresLabel" 属性为 TOC 命名主序列。
# 现在，此 TOC 只会从其 "SequenceIdentifier" 设置为 "MySequence" 的 SEQ 域创建条目。
field_toc.table_of_figures_label = 'MySequence'
# 我们可以在 "PrefixedSequenceIdentifier" 属性中为另一个 SEQ 域序列命名。
# 来自此前缀序列的 SEQ 域将不会创建 TOC 条目。
# 现在，从主序列 SEQ 域创建的每个 TOC 条目还将显示计数
# 前缀序列当前位于生成该条目的主序列 SEQ 字段上。
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# 每个目录条目将在左侧立即显示前缀序列计数
# 页面编号的左侧，即主序列 SEQ 字段出现的页码。
# 我们可以指定一个自定义分隔符，以显示在这两个数字之间。
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 使用 SEQ 字段填充此目录有两种方法。
# 1 - 插入属于目录前缀序列的 SEQ 字段：
# 此字段将把 "PrefixSequence" 的 SEQ 序列计数增加 1。
# 由于此字段不属于已标识的主序列
# 由目录的 "TableOfFiguresLabel" 属性标识，它将不会作为条目出现。
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - 插入属于目录主序列的 SEQ 字段：
# 此 SEQ 字段将在目录中创建一个条目。
# 目录条目将包含 SEQ 字段所在的段落以及它出现的页码。
# 此条目还将显示当前前缀序列的计数，
# 该计数与页码之间由目录的 SeqenceSeparator 属性的值分隔。
# "PrefixSequence" 计数为 1，主序列 SEQ 字段位于第 2 页，
# 分隔符为 ">"，因此条目将显示为 "1>2"。
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# 插入一页，将前缀序列前进 2，并随后插入 SEQ 字段以创建目录条目。
# 前缀序列现在为 2，主序列 SEQ 字段位于第 3 页，
# 因此目录条目将在页码处显示 "2>3"。
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

