---
title: FieldRevNum class
linktitle: FieldRevNum class
articleTitle: FieldRevNum class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldRevNum class. Implements the REVNUM field"
type: docs
weight: 880
url: /python-net/aspose.words.fields/fieldrevnum/
---

## FieldRevNum class

Implements the REVNUM field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the document's revision number, as recorded in the **Revision** property of the
built-in document properties.



**Inheritance:** [FieldRevNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldRevNum()](./__init__/#default) | The default constructor. |

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

Shows how to work with REVNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Current revision #")

# Insert a REVNUM field, which displays the document's current revision number property.
field = builder.insert_field(aw.fields.FieldType.FIELD_REVISION_NUM, True).as_field_rev_num()

self.assertEqual(" REVNUM ", field.get_field_code())
self.assertEqual("1", field.result)
self.assertEqual(1, doc.built_in_document_properties.revision_number)

# This property counts how many times a document has been saved in Microsoft Word,
# and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
# via Properties -> Details. We can update this property manually.
doc.built_in_document_properties.revision_number += 1
field.update()

self.assertEqual("2", field.result)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

