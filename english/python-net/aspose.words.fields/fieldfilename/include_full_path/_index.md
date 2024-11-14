---
title: FieldFileName.include_full_path property
linktitle: include_full_path property
articleTitle: include_full_path property
second_title: Aspose.Words for Python
description: "FieldFileName.include_full_path property. Gets or sets whether to include the full file path name."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldfilename/include_full_path/
---

## FieldFileName.include_full_path property

Gets or sets whether to include the full file path name.


```python
@property
def include_full_path(self) -> bool:
    ...

@include_full_path.setter
def include_full_path(self, value: bool):
    ...

```

### Examples

Shows how to use FieldOptions to override the default value for the FILENAME field.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln()
# This FILENAME field will display the local system file name of the document we loaded.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_NAME, update_field=True).as_field_file_name()
field.update()
self.assertEqual(' FILENAME ', field.get_field_code())
self.assertEqual('Document.docx', field.result)
builder.writeln()
# By default, the FILENAME field shows the file's name, but not its full local file system path.
# We can set a flag to make it show the full file path.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_NAME, update_field=True).as_field_file_name()
field.include_full_path = True
field.update()
self.assertEqual(MY_DIR + 'Document.docx', field.result)
# We can also set a value for this property to
# override the value that the FILENAME field displays.
doc.field_options.file_name = 'FieldOptions.FILENAME.docx'
field.update()
self.assertEqual(' FILENAME  \\p', field.get_field_code())
self.assertEqual('FieldOptions.FILENAME.docx', field.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + doc.field_options.file_name)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFileName](../)

