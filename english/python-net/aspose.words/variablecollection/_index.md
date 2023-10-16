---
title: VariableCollection class
linktitle: VariableCollection class
articleTitle: VariableCollection class
second_title: Aspose.Words for Python
description: "aspose.words.VariableCollection class. A collection of document variables"
type: docs
weight: 1310
url: /python-net/aspose.words/variablecollection/
---

## VariableCollection class

A collection of document variables.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/python-net/work-with-document-properties/) documentation article.




Variable names and values are strings.

Variable names are case-insensitive.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets a document variable at the specified index. ``None`` values are not allowed as a right hand side of the assignment and will be replaced by empty string. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(name, value)](./add/#str_str) | Adds a document variable to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ contains(name)](./contains/#str) | Determines whether the collection contains a document variable with the given name. |
|[ get_by_name(name)](./get_by_name/#str) | Gets or a sets a document variable by the case-insensitive name. ``None`` values are not allowed as a right hand side of the assignment and will be replaced by empty string. |
|[ index_of_key(name)](./index_of_key/#str) | Returns the zero-based index of the specified document variable in the collection. |
|[ remove(name)](./remove/#str) | Removes a document variable with the specified name from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a document variable at the specified index. |

### Examples

Shows how to work with a document's variable collection.

```python
doc = aw.Document()
variables = doc.variables

# Every document has a collection of key/value pair variables, which we can add items to.
variables.add("Home address", "123 Main St.")
variables.add("City", "London")
variables.add("Bedrooms", "3")

self.assertEqual(3, variables.count)

# We can display the values of variables in the document body using DOCVARIABLE fields.
builder = aw.DocumentBuilder(doc)
field = builder.insert_field(aw.fields.FieldType.FIELD_DOC_VARIABLE, True)
field = field.as_field_doc_variable()
field.variable_name = "Home address"
field.update()

self.assertEqual("123 Main St.", field.result)

# Assigning values to existing keys will update them.
variables.add("Home address", "456 Queen St.")

# We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
self.assertEqual("123 Main St.", field.result)

field.update()

self.assertEqual("456 Queen St.", field.result)

# Verify that the document variables with a certain name or value exist.
self.assertTrue(variables.contains("City"))
self.assertTrue(any(str(var) == "London" for var in variables))

# The collection of variables automatically sorts variables alphabetically by name.
self.assertEqual(0, variables.index_of_key("Bedrooms"))
self.assertEqual(1, variables.index_of_key("City"))
self.assertEqual(2, variables.index_of_key("Home address"))

# Enumerate over the collection of variables.
for entry in doc.variables:
    print(f"Name: {entry.key}, Value: {entry.value}")

# Below are three ways of removing document variables from a collection.
# 1 -  By name:
variables.remove("City")

self.assertFalse(variables.contains("City"))

# 2 -  By index:
variables.remove_at(1)

self.assertFalse(variables.contains("Home address"))

# 3 -  Clear the whole collection at once:
variables.clear()

self.assertEqual(0, variables.count)
```

### See Also

* module [aspose.words](../)

