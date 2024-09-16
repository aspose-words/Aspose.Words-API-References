---
title: FieldTemplate class
linktitle: FieldTemplate class
articleTitle: FieldTemplate class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldTemplate class. Implements the TEMPLATE field"
type: docs
weight: 1030
url: /python-net/aspose.words.fields/fieldtemplate/
---

## FieldTemplate class

Implements the TEMPLATE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the file name of the template used by the current document.


**Inheritance:** [FieldTemplate](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldTemplate()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [include_full_path](./include_full_path/) | Gets or sets whether to include the full file path name. |
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

Shows how to use a TEMPLATE field to display the local file system location of a document's template.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# We can set a template name using by the fields. This property is used when the "doc.AttachedTemplate" is empty.
# If this property is empty the default template file name "Normal.dotm" is used.
doc.field_options.template_name = ''
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TEMPLATE, update_field=False).as_field_template()
self.assertEqual(' TEMPLATE ', field.get_field_code())
builder.writeln()
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TEMPLATE, update_field=False).as_field_template()
field.include_full_path = True
self.assertEqual(' TEMPLATE  \\p', field.get_field_code())
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TEMPLATE.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

