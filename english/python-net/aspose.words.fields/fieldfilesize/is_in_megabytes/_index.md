---
title: is_in_megabytes property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets whether to display the file size in megabytes."
type: docs
weight: 30
url: /python-net/aspose.words.fields/fieldfilesize/is_in_megabytes/
---

## FieldFileSize.is_in_megabytes property

Gets or sets whether to display the file size in megabytes.


### Examples

Shows how to display the file size of a document with a FILESIZE field.

```python
doc = aw.Document(MY_DIR + "Document.docx")

self.assertEqual(18105, doc.built_in_document_properties.bytes)

builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.insert_paragraph()

# Below are three different units of measure
# with which FILESIZE fields can display the document's file size.
# 1 -  Bytes:
field = builder.insert_field(aw.fields.FieldType.FIELD_FILE_SIZE, True).as_field_file_size()
field.update()

self.assertEqual(" FILESIZE ", field.get_field_code())
self.assertEqual("18105", field.result)

# 2 -  Kilobytes:
builder.insert_paragraph()
field = builder.insert_field(aw.fields.FieldType.FIELD_FILE_SIZE, True).as_field_file_size()
field.is_in_kilobytes = True
field.update()

self.assertEqual(" FILESIZE  \\k", field.get_field_code())
self.assertEqual("18", field.result)

# 3 -  Megabytes:
builder.insert_paragraph()
field = builder.insert_field(aw.fields.FieldType.FIELD_FILE_SIZE, True).as_field_file_size()
field.is_in_megabytes = True
field.update()

self.assertEqual(" FILESIZE  \\m", field.get_field_code())
self.assertEqual("0", field.result)

# To update the values of these fields while editing in Microsoft Word,
# we must first save the changes, and then manually update these fields.
doc.save(ARTIFACTS_DIR + "Field.field_file_size.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFileSize](../)

