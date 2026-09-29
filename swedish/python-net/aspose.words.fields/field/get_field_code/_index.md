---
title: Field.get_field_code method
linktitle: get_field_code method
articleTitle: get_field_code method
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field.get_field_code method"
type: docs
weight: 1060
url: /sv/python-net/aspose.words.fields/field/get_field_code/
---

## get_field_code() {#default}

Returns text between field start and field separator (or field end if there is no separator).
Both field code and field result of child fields are included.


```python
def get_field_code(self):
    ...
```

## get_field_code(include_child_field_codes) {#bool}

Returns text between field start and field separator (or field end if there is no separator).


```python
def get_field_code(self, include_child_field_codes: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| include_child_field_codes | bool | ``True`` if child field codes should be included. |

## Examples

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
field = builder.insert_field('DATE \\@ "dddd, MMMM dd, yyyy"')
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
# Denna överlagring av metoden "insert_field" uppdaterar automatiskt infogade fält.
self.assertAlmostEqual(datetime.datetime.strptime(field.result, '%A, %B %d, %Y'), datetime.datetime.now(), delta=timedelta(1))
```

Shows how to get a field's field code.

```python
# Öppna ett dokument som innehåller ett MERGEFIELD inuti ett IF-fält.
doc = aw.Document(file_name=MY_DIR + 'Nested fields.docx')
field_if = doc.range.fields[0].as_field_if()
# Det finns två sätt att hämta ett fälts fältkod:
# 1 -  Utelämna dess inre fält:
self.assertEqual(' IF  > 0 " (surplus of ) " "" ', field_if.get_field_code(False))
# 2 -  Inkludera dess inre fält:
self.assertEqual(f' IF \x13 MERGEFIELD NetIncome \x14\x15 > 0 " (surplus of \x13 MERGEFIELD  NetIncome \\f $ \x14\x15) " "" ', field_if.get_field_code(True))
# Som standard visar metoden GetFieldCode inre fält.
self.assertEqual(field_if.get_field_code(), field_if.get_field_code(True))
```

## See Also

* module [aspose.words.fields](../../)
* class [Field](../)

