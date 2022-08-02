---
title: FieldLastSavedBy class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the LASTSAVEDBY field."
type: docs
weight: 640
url: /python-net/aspose.words.fields/fieldlastsavedby/
---

## FieldLastSavedBy class

Implements the LASTSAVEDBY field.


Retrieves the name of the user who last modified and saved the current document, as recorded in the **LastModifiedBy**
property of the built-in document properties.



**Inheritance:** [FieldLastSavedBy](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldLastSavedBy()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use the LASTSAVEDBY field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we create a document in Microsoft Word, it will have the user's name in the "Last saved by" built-in property.
# If we make a document programmatically, this property will be null, and we will need to assign a value.
doc.built_in_document_properties.last_saved_by = "John Doe"

# We can use the LASTSAVEDBY field to display the value of this property in the document.
field = builder.insert_field(aw.fields.FieldType.FIELD_LAST_SAVED_BY, True).as_field_last_saved_by()

self.assertEqual(" LASTSAVEDBY ", field.get_field_code())
self.assertEqual("John Doe", field.result)

doc.save(ARTIFACTS_DIR + "Field.field_last_saved_by.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

