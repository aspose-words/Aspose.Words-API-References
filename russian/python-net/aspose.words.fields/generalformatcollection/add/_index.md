---
title: GeneralFormatCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "GeneralFormatCollection.add method. Adds a general format to the collection."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/generalformatcollection/add/
---

## add(item) {#generalformat}

Adds a general format to the collection.


```python
def add(self, item: aspose.words.fields.GeneralFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| item | [GeneralFormat](../../generalformat/) | A general format. |

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Используйте DocumentBuilder, чтобы вставить поле, отображающее результат без применения формата.
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# Мы можем применить формат к результату поля, используя свойства поля.
# Ниже представлены три типа форматов, которые мы можем применить к результату поля.
# 1 -  Числовой формат:
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Формат даты/времени:
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 -  Общий формат:
field = builder.insert_field(field_code='= 25 + 33')
format_obj = field.format
format_obj.general_formats.add(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.add(aw.fields.GeneralFormat.UPPER)
field.update()
index = 0
for general_format in format_obj.general_formats:
    print(f'General format index {index}: {general_format}')
    index += 1
self.assertEqual('= 25 + 33 \\* roman \\* Upper', field.get_field_code())
self.assertEqual('LVIII', field.result)
self.assertEqual(2, len(format_obj.general_formats))
self.assertEqual(aw.fields.GeneralFormat.LOWERCASE_ROMAN, format_obj.general_formats[0])
# Мы можем удалить наши форматы, чтобы вернуть результат поля к его исходному виду.
format_obj.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.remove_at(0)
self.assertEqual(0, len(format_obj.general_formats))
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, len(format_obj.general_formats))
```

### See Also

* module [aspose.words.fields](../../)
* class [GeneralFormatCollection](../)

