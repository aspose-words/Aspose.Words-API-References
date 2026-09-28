---
title: FieldFileSize.is_in_megabytes property
linktitle: is_in_megabytes property
articleTitle: is_in_megabytes property
second_title: Aspose.Words for Python
description: "FieldFileSize.is_in_megabytes property. Gets or sets whether to display the file size in megabytes."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldfilesize/is_in_megabytes/
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
# 以下是三种不同的计量单位
# 用于 FILESIZE 字段显示文档的文件大小。
# 1 -  字节：
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.update()
self.assertEqual(' FILESIZE ', field.get_field_code())
self.assertEqual('18105', field.result)
# 2 -  千字节：
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.is_in_kilobytes = True
field.update()
self.assertEqual(' FILESIZE  \\k', field.get_field_code())
self.assertEqual('18', field.result)
# 3 -  兆字节：
builder.insert_paragraph()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_FILE_SIZE, update_field=True).as_field_file_size()
field.is_in_megabytes = True
field.update()
self.assertEqual(' FILESIZE  \\m', field.get_field_code())
self.assertEqual('0', field.result)
# 要在 Microsoft Word 中编辑时更新这些字段的值，
# 我们必须先保存更改，然后手动更新这些字段。
doc.save(file_name=ARTIFACTS_DIR + 'Field.FILESIZE.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldFileSize](../)

