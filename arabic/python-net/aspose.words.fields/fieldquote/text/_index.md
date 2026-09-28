---
title: FieldQuote.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldQuote.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldquote/text/
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
# أدرج حقل QUOTE، الذي سيعرض قيمة خاصية Text الخاصة به.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# أدرج حقل QUOTE وضع داخله حقل DATE.
# حقول DATE تُحدّث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
# وضع حقل DATE داخل حقل QUOTE بهذه الطريقة سيجمد قيمته
# إلى التاريخ الذي أنشأنا فيه المستند.
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# حدّث جميع الحقول لعرض نتائجها الصحيحة.
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldQuote](../)

