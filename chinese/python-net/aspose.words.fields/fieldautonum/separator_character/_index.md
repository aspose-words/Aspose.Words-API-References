---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 每个 AUTONUM 字段显示 AUTONUM 字段运行计数的当前值，
# 允许我们自动为项目编号，就像有序列表一样。
# 此字段将显示数字 "1."。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# 分隔符字符默认是句点，它出现在字段结果中数字后面。
# 如果我们将此属性设为 null，我们的第二个 AUTONUM 字段将在文档中显示 "2."。
self.assertIsNone(field.separator_character)
# 我们可以设置此属性，以将其字符串的第一个字符用作新的分隔符字符。
# 在这种情况下，我们的 AUTONUM 字段现在将显示 "2:"。
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

