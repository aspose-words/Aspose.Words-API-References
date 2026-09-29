---
title: FieldFormat.general_formats property
linktitle: general_formats property
articleTitle: general_formats property
second_title: Aspose.Words for Python
description: "FieldFormat.general_formats property. Gets a collection of general formats that are applied to a numeric, text or any field result"
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fieldformat/general_formats/
---

## FieldFormat.general_formats property

Gets a collection of general formats that are applied to a numeric, text or any field result.
Corresponds to the \\\* switches.


```python
@property
def general_formats(self) -> aspose.words.fields.GeneralFormatCollection:
    ...

```

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Usa un document builder per inserire un campo che visualizza un risultato senza alcun formato applicato.
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# Possiamo applicare un formato al risultato di un campo usando le proprietà del campo.
# Di seguito sono riportati tre tipi di formati che possiamo applicare al risultato di un campo.
# 1 -  Formato numerico:
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Formato data/ora:
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 -  Formato generale:
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
# Possiamo rimuovere i nostri formati per ripristinare il risultato del campo nella sua forma originale.
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
* class [FieldFormat](../)

