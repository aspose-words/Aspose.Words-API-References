---
title: FieldSeq.reset_heading_level property
linktitle: reset_heading_level property
articleTitle: reset_heading_level property
second_title: Aspose.Words for Python
description: "FieldSeq.reset_heading_level property. Gets or sets an integer number representing a heading level to reset the sequence number to"
type: docs
weight: 40
url: /zh/python-net/aspose.words.fields/fieldseq/reset_heading_level/
---

## FieldSeq.reset_heading_level property

Gets or sets an integer number representing a heading level to reset the sequence number to.
Returns -1 if the number is absent.


```python
@property
def reset_heading_level(self) -> str:
    ...

@reset_heading_level.setter
def reset_heading_level(self, value: str):
    ...

```

### Examples

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# SEQ 域显示一个在每个 SEQ 域递增的计数。
# 这些域还为每个唯一命名的序列维护单独的计数
# 由 SEQ 域的 "SequenceIdentifier" 属性标识。
# 插入一个 SEQ 字段，以显示 "MySequence" 的当前计数值，
# 在使用 "ResetNumber" 属性将其设置为 100 之后。
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# 使用另一个 SEQ 字段显示此序列的下一个数字。
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# 插入一级标题。
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# 插入同一序列的另一个 SEQ 字段，并将其配置为在每个标题处将计数重置为 1。
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# 上述标题是一级标题，因此此序列的计数被重置为 1。
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# 移动到此序列的下一个数字。
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

