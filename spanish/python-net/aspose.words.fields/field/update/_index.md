---
title: Field.update method
linktitle: update method
articleTitle: update method
second_title: Aspose.Words for Python
description: "aspose.words.fields.Field.update method"
type: docs
weight: 1090
url: /es/python-net/aspose.words.fields/field/update/
---

## update() {#default}

Performs the field update. Throws if the field is being updated already.


```python
def update(self):
    ...
```

## update(ignore_merge_format) {#bool}

Performs a field update. Throws if the field is being updated already.


```python
def update(self, ignore_merge_format: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ignore_merge_format | bool | If ``True`` then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

## Examples

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

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
include_picture = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INCLUDE_PICTURE, update_field=True).as_field_include_picture()
include_picture.source_full_name = IMAGE_DIR + 'Transparent background logo.png'
include_picture.update(True)
with io.BytesIO() as doc_stream:
    doc.save(stream=doc_stream, save_options=aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX))
    # Podemos establecer una bandera en un objeto LoadOptions para decidir si convertir todos los campos INCLUDEPICTURE
    # en formas de imagen al cargar un documento que los contenga.
    load_options = aw.loading.LoadOptions()
    load_options.preserve_include_picture_field = preserve_include_picture_field
    doc = aw.Document(stream=doc_stream, load_options=load_options)
    if preserve_include_picture_field:
        self.assertTrue(any([f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE for f in doc.range.fields]))
        doc.update_fields()
        doc.save(file_name=ARTIFACTS_DIR + 'Field.PreserveIncludePicture.docx')
    else:
        self.assertFalse(any([f.type == aw.fields.FieldType.FIELD_INCLUDE_PICTURE for f in doc.range.fields]))
```

## See Also

* module [aspose.words.fields](../../)
* class [Field](../)

