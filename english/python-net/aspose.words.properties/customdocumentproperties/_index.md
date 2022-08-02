---
title: CustomDocumentProperties class
second_title: Aspose.Words for Python via .NET API Reference
description: "A collection of custom document properties."
type: docs
weight: 20
url: /python-net/aspose.words.properties/customdocumentproperties/
---

## CustomDocumentProperties class

A collection of custom document properties.


Each [DocumentProperty](../documentproperty/) object represents a custom property of a container document.




The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




**Inheritance:** [CustomDocumentProperties](./) → [DocumentPropertyCollection](../documentpropertycollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) |  |

### Properties

| Name | Description |
| --- | --- |
| [count](../documentpropertycollection/count/) | Gets number of items in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(name, value)](./add/#str_str) | Creates a new custom document property of the **PropertyType.String** data type. |
|[ add(name, value)](./add/#str_int) | Creates a new custom document property of the **PropertyType.Number** data type. |
|[ add(name, value)](./add/#str_datetime) | Creates a new custom document property of the **PropertyType.DateTime** data type. |
|[ add(name, value)](./add/#str_bool) | Creates a new custom document property of the **PropertyType.Boolean** data type. |
|[ add(name, value)](./add/#str_float) | Creates a new custom document property of the **PropertyType.Float** data type. |
|[ add_link_to_content(name, link_source)](./add_link_to_content/#str_str) | Creates a new linked to content custom document property. |
|[ clear()](../documentpropertycollection/clear/#default) | Removes all properties from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ contains(name)](../documentpropertycollection/contains/#str) | Returns true if a property with the specified name exists in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ get_by_name(name)](../documentpropertycollection/get_by_name/#str) | Returns a [DocumentProperty](../documentproperty/) object by the name of the property.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ index_of(name)](../documentpropertycollection/index_of/#str) | Gets the index of a property by name.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove(name)](../documentpropertycollection/remove/#str) | Removes a property with the specified name from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove_at(index)](../documentpropertycollection/remove_at/#int) | Removes a property at the specified index.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

### Examples

Shows how to work with custom document properties.

```python
doc = aw.Document(MY_DIR + "Properties.docx")

# Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
# The document has a fixed list of built-in properties. The user creates all of the custom properties.
self.assertEqual("Value of custom document property", str(doc.custom_document_properties.get_by_name("CustomProperty")))

doc.custom_document_properties.add("CustomProperty2", "Value of custom document property #2")

print("Custom Properties:")
for custom_document_property in doc.custom_document_properties:
    print(custom_document_property.name)
    print(f"\tType:\t{custom_document_property.type}")
    print(f"\tValue:\t\"{custom_document_property.value}\"")
```

### See Also

* module [aspose.words.properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* class [Document](../../aspose.words/document/)
* property [Document.built_in_document_properties](../../aspose.words/document/built_in_document_properties/)
* property [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/)

