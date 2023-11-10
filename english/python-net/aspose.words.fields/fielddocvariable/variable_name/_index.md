---
title: FieldDocVariable.variable_name property
linktitle: variable_name property
articleTitle: variable_name property
second_title: Aspose.Words for Python
description: "FieldDocVariable.variable_name property. Gets or sets the name of the document variable to retrieve."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fielddocvariable/variable_name/
---

## FieldDocVariable.variable_name property

Gets or sets the name of the document variable to retrieve.


```python
@property
def variable_name(self) -> str:
    ...

@variable_name.setter
def variable_name(self, value: str):
    ...

```

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

* module [aspose.words.fields](../../)
* class [FieldDocVariable](../)

