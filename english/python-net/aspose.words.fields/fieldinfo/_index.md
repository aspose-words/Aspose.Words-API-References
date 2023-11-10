---
title: FieldInfo class
linktitle: FieldInfo class
articleTitle: FieldInfo class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldInfo class. Implements the INFO field"
type: docs
weight: 620
url: /python-net/aspose.words.fields/fieldinfo/
---

## FieldInfo class

Implements the INFO field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts information about a document property.


**Inheritance:** [FieldInfo](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldInfo()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [info_type](./info_type/) | Gets or sets the type of the document property to insert. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [new_value](./new_value/) | Gets or sets an optional value that updates the property. |
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

Shows how to work with INFO fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Set a value for the "comments" built-in property and then insert an INFO field to display that property's value.
doc.built_in_document_properties.comments = "My comment"
field = builder.insert_field(aw.fields.FieldType.FIELD_INFO, True).as_field_info()
field.info_type = "Comments"
field.update()

self.assertEqual(" INFO  Comments", field.get_field_code())
self.assertEqual("My comment", field.result)

builder.writeln()

# Setting a value for the field's "new_value" property and updating
# the field will also overwrite the corresponding built-in property with the new value.
field = builder.insert_field(aw.fields.FieldType.FIELD_INFO, True).as_field_info()
field.info_type = "Comments"
field.new_value = "New comment"
field.update()

self.assertEqual(" INFO  Comments \"New comment\"", field.get_field_code())
self.assertEqual("New comment", field.result)
self.assertEqual("New comment", doc.built_in_document_properties.comments)

doc.save(ARTIFACTS_DIR + "Field.field_info.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

