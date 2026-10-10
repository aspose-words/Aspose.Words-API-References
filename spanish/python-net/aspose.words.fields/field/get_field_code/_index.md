---
title: Field.get_field_code method
linktitle: get_field_code method
articleTitle: get_field_code method
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field.get_field_code method"
type: docs
weight: 1060
url: /es/python-net/aspose.words.fields/field/get_field_code/
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
# Esta sobrecarga del método "insert_field" actualiza automáticamente los campos insertados.
self.assertAlmostEqual(datetime.datetime.strptime(field.result, '%A, %B %d, %Y'), datetime.datetime.now(), delta=timedelta(1))
```

Shows how to get a field's field code.

```python
# Abra un documento que contenga un MERGEFIELD dentro de un campo IF.
doc = aw.Document(file_name=MY_DIR + 'Nested fields.docx')
field_if = doc.range.fields[0].as_field_if()
# Hay dos formas de obtener el código de campo de un campo:
# 1 -  Omitir sus campos internos:
self.assertEqual(' IF  > 0 " (surplus of ) " "" ', field_if.get_field_code(False))
# 2 -  Incluir sus campos internos:
self.assertEqual(f' IF \x13 MERGEFIELD NetIncome \x14\x15 > 0 " (surplus of \x13 MERGEFIELD  NetIncome \\f $ \x14\x15) " "" ', field_if.get_field_code(True))
# Por defecto, el método GetFieldCode muestra los campos internos.
self.assertEqual(field_if.get_field_code(), field_if.get_field_code(True))
```

## See Also

* module [aspose.words.fields](../../)
* class [Field](../)

