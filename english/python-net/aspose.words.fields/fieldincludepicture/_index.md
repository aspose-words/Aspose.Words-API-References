---
title: FieldIncludePicture class
linktitle: FieldIncludePicture class
articleTitle: FieldIncludePicture class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIncludePicture class. Implements the INCLUDEPICTURE field"
type: docs
weight: 580
url: /python-net/aspose.words.fields/fieldincludepicture/
---

## FieldIncludePicture class

Implements the INCLUDEPICTURE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves a picture and displays it as the field result.


**Inheritance:** [FieldIncludePicture](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldIncludePicture()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [graphic_filter](./graphic_filter/) | Gets or sets the name of the filter for the format of the graphic that is to be inserted. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_linked](./is_linked/) | Gets or sets whether to reduce the file size by not storing graphics data with the document. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [resize_horizontally](./resize_horizontally/) | Gets or sets whether to resize the picture horizontally from the source. |
| [resize_vertically](./resize_vertically/) | Gets or sets whether to resize the picture vertically from the source. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [source_full_name](./source_full_name/) | Gets or sets the location of the picture using an IRI. |
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

Shows how to insert images using IMPORT and INCLUDEPICTURE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two similar field types that we can use to display images linked from the local file system.
# 1 -  The INCLUDEPICTURE field:
field_include_picture = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE_PICTURE, True).as_field_include_picture()
field_include_picture.source_full_name = IMAGE_DIR + "Transparent background logo.png"

self.assertRegex(field_include_picture.get_field_code(), " INCLUDEPICTURE  .*")

# Apply the PNG32.FLT filter.
field_include_picture.graphic_filter = "PNG32"
field_include_picture.is_linked = True
field_include_picture.resize_horizontally = True
field_include_picture.resize_vertically = True

# 2 -  The IMPORT field:
field_import = builder.insert_field(aw.fields.FieldType.FIELD_IMPORT, True).as_field_import()
field_import.source_full_name = IMAGE_DIR + "Transparent background logo.png"
field_import.graphic_filter = "PNG32"
field_import.is_linked = True

self.assertRegex(field_import.get_field_code(), r" IMPORT  .* \\c PNG32 \\d")

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_include_picture.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

