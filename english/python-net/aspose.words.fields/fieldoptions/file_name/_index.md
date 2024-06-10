---
title: FieldOptions.file_name property
linktitle: file_name property
articleTitle: file_name property
second_title: Aspose.Words for Python
description: "FieldOptions.file_name property. Gets or sets the file name of the document."
type: docs
weight: 140
url: /python-net/aspose.words.fields/fieldoptions/file_name/
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
doc = aw.Document(MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln()
# This FILENAME field will display the local system file name of the document we loaded.
field = builder.insert_field(aw.fields.FieldType.FIELD_FILE_NAME, True).as_field_file_name()
field.update()
self.assertEqual(' FILENAME ', field.get_field_code())
self.assertEqual('Document.docx', field.result)
builder.writeln()
# By default, the FILENAME field shows the file's name, but not its full local file system path.
# We can set a flag to make it show the full file path.
field = builder.insert_field(aw.fields.FieldType.FIELD_FILE_NAME, True).as_field_file_name()
field.include_full_path = True
field.update()
self.assertEqual(MY_DIR + 'Document.docx', field.result)
# We can also set a value for this property to
# override the value that the FILENAME field displays.
doc.field_options.file_name = 'FieldOptions.file_name.docx'
field.update()
self.assertEqual(' FILENAME  \\p', field.get_field_code())
self.assertEqual('FieldOptions.file_name.docx', field.result)
doc.update_fields()
doc.save(ARTIFACTS_DIR + doc.field_options.file_name)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

