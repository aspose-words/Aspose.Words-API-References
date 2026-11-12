---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fields/fieldautonum/separator_character/
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
# Каждое поле AUTONUM отображает текущее значение текущего счёта полей AUTONUM,
# позволяя нам автоматически нумеровать элементы, как в нумерованном списке.
# Это поле будет отображать номер "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# Символ-разделитель, который появляется в результате поля сразу после числа, по умолчанию является точкой.
# Если оставить это свойство null, наше второе поле AUTONUM отобразит "2." в документе.
self.assertIsNone(field.separator_character)
# Мы можем установить это свойство, чтобы первый символ его строки использовался в качестве нового символа-разделителя.
# В этом случае наше поле AUTONUM теперь будет отображать "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

