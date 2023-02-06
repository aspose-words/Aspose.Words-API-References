---
title: FieldFileSize class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the FILESIZE field"
type: docs
weight: 420
url: /python-net/aspose.words.fields/fieldfilesize/
---

## FieldFileSize class

Implements the FILESIZE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the size of the current document's file or 0 if the size cannot be determined.

In the current implementation, uses the [Document.original_file_name](../../aspose.words/document/original_file_name/) property to retrieve
the file name used to determine the file size.




**Inheritance:** [FieldFileSize](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldFileSize()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_in_kilobytes](./is_in_kilobytes/) | Gets or sets whether to display the file size in kilobytes. |
| [is_in_megabytes](./is_in_megabytes/) | Gets or sets whether to display the file size in megabytes. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

* module [aspose.words.fields](../)
* class [Field](../field/)

