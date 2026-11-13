---
title: FieldFormat class
linktitle: FieldFormat class
articleTitle: FieldFormat class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldFormat class. Provides typed access to field's numeric, date and time, and general formatting"
type: docs
weight: 480
url: /es/python-net/aspose.words.fields/fieldformat/
---

## FieldFormat class

Provides typed access to field's numeric, date and time, and general formatting.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [date_time_format](./date_time_format/) | Gets or sets a formatting that is applied to a date and time field result. Corresponds to the \\@ switch. |
| [general_formats](./general_formats/) | Gets a collection of general formats that are applied to a numeric, text or any field result. Corresponds to the \\\* switches. |
| [numeric_format](./numeric_format/) | Gets or sets a formatting that is applied to a numeric field result. Corresponds to the \\# switch. |

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Utilice un document builder para insertar un campo que muestre un resultado sin formato aplicado.
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# Podemos aplicar un formato al resultado de un campo usando las propiedades del campo.
# A continuación se presentan tres tipos de formatos que podemos aplicar al resultado de un campo.
# 1 -  Formato numérico:
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Formato de fecha/hora:
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 -  Formato general:
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
# Podemos eliminar nuestros formatos para devolver el resultado del campo a su forma original.
format_obj.general_formats.remove(aw.fields.GeneralFormat.LOWERCASE_ROMAN)
format_obj.general_formats.remove_at(0)
self.assertEqual(0, len(format_obj.general_formats))
field.update()
self.assertEqual('= 25 + 33  ', field.get_field_code())
self.assertEqual('58', field.result)
self.assertEqual(0, len(format_obj.general_formats))
```

### See Also

* module [aspose.words.fields](../)

