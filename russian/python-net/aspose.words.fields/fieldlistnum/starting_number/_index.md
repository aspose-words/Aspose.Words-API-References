---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /ru/python-net/aspose.words.fields/fieldlistnum/starting_number/
---

## FieldListNum.starting_number property

Gets or sets the starting value for this field.


```python
@property
def starting_number(self) -> str:
    ...

@starting_number.setter
def starting_number(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поля LISTNUM отображают число, которое увеличивается в каждом поле LISTNUM.
# Эти поля также имеют разнообразные параметры, позволяющие использовать их для имитации нумерованных списков.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Списки по умолчанию начинают счет с 1, но мы можем установить другое значение, например 0.
# Это поле отобразит "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# Поля LISTNUM поддерживают отдельные счетчики для каждого уровня списка.
# Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
# увеличивает уровень списка вместо счетчика.
# Следующее поле продолжит счет, который мы начали выше, и отобразит значение "1" на уровне списка 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Это поле начнет счет на уровне списка 2. Оно отобразит значение "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Это поле начнет счет на уровне списка 3. Оно отобразит значение "1".
# Разные уровни списка имеют разное форматирование,
# поэтому эти поля вместе отобразят значение "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Следующее поле LISTNUM, которое мы вставим, продолжит счёт на уровне списка
# на котором находилось предыдущее поле LISTNUM.
# Мы можем использовать свойство "ListLevel", чтобы перейти к другому уровню списка.
# Если бы это поле LISTNUM оставалось на уровне списка 3, оно отобразило бы "ii)",
# но, поскольку мы переместили его на уровень списка 2, оно продолжает счёт на этом уровне и отображает "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Мы можем установить свойство ListName, чтобы поле имитировало другой тип поля AUTONUM.
# "NumberDefault" имитирует AUTONUM, "OutlineDefault" имитирует AUTONUMOUT,
# а "LegalDefault" имитирует поля AUTONUMLGL.
# Имя списка "OutlineDefault" с 1 в качестве начального номера приведёт к отображению "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# ListName не переносится от предыдущего поля, поэтому нам придётся задавать его для каждого нового поля.
# Это поле продолжает счёт с другим именем списка и отображает "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

