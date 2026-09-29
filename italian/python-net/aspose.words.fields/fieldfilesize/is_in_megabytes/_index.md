---
title: FieldFileSize.is_in_megabytes property
linktitle: is_in_megabytes property
articleTitle: is_in_megabytes property
second_title: Aspose.Words for Python
description: "FieldFileSize.is_in_megabytes property. Gets or sets whether to display the file size in megabytes."
type: docs
weight: 30
url: /it/python-net/aspose.words.fields/fieldfilesize/is_in_megabytes/
---

## FieldFileSize.is_in_megabytes property

Gets or sets whether to display the file size in megabytes.


```python
@property
def is_in_megabytes(self) -> bool:
    ...

@is_in_megabytes.setter
def is_in_megabytes(self, value: bool):
    ...

```

### Examples

Shows how to display the file size of a document with a FILESIZE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
self.assertEqual(18105, doc.built_in_document_properties.bytes)
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.insert_paragraph()
# Di seguito sono riportate tre diverse unità di misura
# con le quali i campi FILESIZE possono visualizzare la dimensione del file del documento.
# 1 -  Byte:
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.update()
self.assertEqual(' FILESIZE ', field.get_field_code())
self.assertEqual('18105', field.result)
# 2 -  Kilobyte:
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.is_in_kilobytes = True
field.update()
self.assertEqual(' FILESIZE  \\k', field.get_field_code())
self.assertEqual('18', field.result)
# 3 -  Megabyte:
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.is_in_megabytes = True
field.update()
self.assertEqual(' FILESIZE  \\m', field.get_field_code())
self.assertEqual('0', field.result)
# Per aggiornare i valori di questi campi durante la modifica in Microsoft Word,
# dobbiamo prima salvare le modifiche e poi aggiornare manualmente questi campi.
doc.save(file_name=ARTIFACTS_DIR + 'Field.FILESIZE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFileSize](../)

