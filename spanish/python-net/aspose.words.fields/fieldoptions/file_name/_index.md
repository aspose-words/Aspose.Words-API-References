---
title: FieldOptions.file_name property
linktitle: file_name property
articleTitle: file_name property
second_title: Aspose.Words for Python
description: "FieldOptions.file_name property. Gets or sets the file name of the document."
type: docs
weight: 140
url: /es/python-net/aspose.words.fields/fieldoptions/file_name/
---

## FieldOptions.file_name property

Gets or sets the file name of the document.


```python
@property
def file_name(self) -> str:
    ...

@file_name.setter
def file_name(self, value: str):
    ...

```

### Remarks

This property is used by the [FieldFileName](../../fieldfilename/) field with higher priority than the [Document.original_file_name](../../../aspose.words/document/original_file_name/) property.




### Examples

Shows how to use FieldOptions to override the default value for the FILENAME field.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln()
# Este campo FILENAME mostrará el nombre de archivo del sistema local del documento que cargamos.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_NAME, update_field=True).as_field_file_name()
field.update()
self.assertEqual(' FILENAME ', field.get_field_code())
self.assertEqual('Document.docx', field.result)
builder.writeln()
# Por defecto, el campo FILENAME muestra el nombre del archivo, pero no su ruta completa en el sistema de archivos local.
# Podemos establecer una bandera para que muestre la ruta completa del archivo.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_NAME, update_field=True).as_field_file_name()
field.include_full_path = True
field.update()
self.assertEqual(MY_DIR + 'Document.docx', field.result)
# También podemos establecer un valor para esta propiedad a
# sobrescribir el valor que muestra el campo FILENAME.
doc.field_options.file_name = 'FieldOptions.FILENAME.docx'
field.update()
self.assertEqual(' FILENAME  \\p', field.get_field_code())
self.assertEqual('FieldOptions.FILENAME.docx', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + doc.field_options.file_name)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

