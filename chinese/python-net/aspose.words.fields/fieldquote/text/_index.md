---
title: FieldQuote.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldQuote.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldquote/text/
---

## FieldQuote.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个 QUOTE 字段，它将显示其 Text 属性的值。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# 插入一个 QUOTE 字段，并在其中嵌套一个 DATE 字段。
# 每次使用 Microsoft Word 打开文档时，DATE 字段都会将其值更新为当前日期。
# 像这样将 DATE 字段嵌套在 QUOTE 字段中将冻结其值
# 为我们创建文档时的日期。
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# 更新所有字段以显示其正确的结果。
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldQuote](../)

