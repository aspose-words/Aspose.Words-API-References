---
title: FieldSubject class
linktitle: FieldSubject class
articleTitle: FieldSubject class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSubject class. Implements the SUBJECT field"
type: docs
weight: 990
url: /python-net/aspose.words.fields/fieldsubject/
---

## FieldSubject class

Implements the SUBJECT field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves, and optionally sets, the document's subject, as recorded in the **Subject** property of the
built-in document properties.



**Inheritance:** [FieldSubject](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSubject()](./__init__/#default) | The default constructor. |

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
| [text](./text/) | Gets or sets the text of the subject. |
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

Shows how to use the SUBJECT field.

```python
doc = aw.Document()
# Set a value for the document's "subject" built-in property.
doc.built_in_document_properties.subject = 'My subject'
# Create a SUBJECT field to display the value of that built-in property.
builder = aw.DocumentBuilder(doc)
field = builder.insert_field(aw.fields.FieldType.FIELD_SUBJECT, True).as_field_subject()
field.update()
self.assertEqual(' SUBJECT ', field.get_field_code())
self.assertEqual('My subject', field.result)
# If we give the SUBJECT field's "text" property value and update it, the field will
# overwrite the current value of the "subject" built-in property with the value of its Text property,
# and then display the new value.
field.text = 'My new subject'
field.update()
self.assertEqual(' SUBJECT  "My new subject"', field.get_field_code())
self.assertEqual('My new subject', field.result)
self.assertEqual('My new subject', doc.built_in_document_properties.subject)
doc.save(ARTIFACTS_DIR + 'Field.field_subject.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

