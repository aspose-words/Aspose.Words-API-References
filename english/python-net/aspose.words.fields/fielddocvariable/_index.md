---
title: FieldDocVariable class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements DOCVARIABLE field"
type: docs
weight: 360
url: /python-net/aspose.words.fields/fielddocvariable/
---

## FieldDocVariable class

Implements DOCVARIABLE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.




**Inheritance:** [FieldDocVariable](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldDocVariable()](./__init__/#default) | The default constructor. |

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
| [variable_name](./variable_name/) | Gets or sets the name of the document variable to retrieve. |

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

Shows how to use DOCPROPERTY fields to display document properties and variables.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two ways of using DOCPROPERTY fields.
# 1 -  Display a built-in property:
# Set a custom value for the "category" built-in property, then insert a DOCPROPERTY field that references it.
doc.built_in_document_properties.category = "My category"

field_doc_property = builder.insert_field(" DOCPROPERTY Category ").as_field_doc_property()
field_doc_property.update()

self.assertEqual(" DOCPROPERTY Category ", field_doc_property.get_field_code())
self.assertEqual("My category", field_doc_property.result)

builder.insert_paragraph()

# 2 -  Display a custom document variable:
# Define a custom variable, then reference that variable with a DOCPROPERTY field.
self.assertEqual(0, len(list(doc.variables)))
doc.variables.add("My variable", "My variable's value")

field_doc_variable = builder.insert_field(aw.fields.FieldType.FIELD_DOC_VARIABLE, True).as_field_doc_variable()
field_doc_variable.variable_name = "My Variable"
field_doc_variable.update()

self.assertEqual(" DOCVARIABLE  \"My Variable\"", field_doc_variable.get_field_code())
self.assertEqual("My variable's value", field_doc_variable.result)

doc.save(ARTIFACTS_DIR + "Field.field_doc_variable.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

