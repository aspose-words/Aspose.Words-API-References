---
title: GeneralFormatCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "GeneralFormatCollection.count property. Gets the total number of the items in the collection."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/generalformatcollection/count/
---

## GeneralFormatCollection.count property

Gets the total number of the items in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how to format field results.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Verwenden Sie einen Document Builder, um ein Feld einzufügen, das ein Ergebnis ohne angewendetes Format anzeigt.
field = builder.insert_field(field_code='= 2 + 3')
self.assertEqual('= 2 + 3', field.get_field_code())
self.assertEqual('5', field.result)
# Wir können ein Format auf das Ergebnis eines Feldes anwenden, indem wir die Eigenschaften des Feldes verwenden.
# Unten sind drei Arten von Formaten aufgeführt, die wir auf das Ergebnis eines Feldes anwenden können.
# 1 -  Numerisches Format:
format_obj = field.format
format_obj.numeric_format = '$###.00'
field.update()
self.assertEqual('= 2 + 3 \\# $###.00', field.get_field_code())
self.assertEqual('$  5.00', field.result)
# 2 -  Datums-/Uhrzeitformat:
field = builder.insert_field(field_code='DATE')
format_obj = field.format
format_obj.date_time_format = 'dddd, MMMM dd, yyyy'
field.update()
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
print(f"Today's date, in {format_obj.date_time_format} format:\n\t{field.result}")
# 3 -  Allgemeines Format:
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
# Wir können unsere Formate entfernen, um das Ergebnis des Feldes in seine ursprüngliche Form zurückzusetzen.
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

