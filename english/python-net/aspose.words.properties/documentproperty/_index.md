---
title: DocumentProperty class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a custom or built-in document property."
type: docs
weight: 30
url: /python-net/aspose.words.properties/documentproperty/
---

## DocumentProperty class

Represents a custom or built-in document property.


### Properties

| Name | Description |
| --- | --- |
| [is_link_to_content](./is_link_to_content/) | Shows whether this property is linked to content or not. |
| [link_source](./link_source/) | Gets the source of a linked custom document property. |
| [name](./name/) | Returns the name of the property. |
| [type](./type/) | Gets the data type of the property. |
| [value](./value/) | Gets or sets the value of the property. |

### Methods

| Name | Description |
| --- | --- |
|[ to_bool()](./to_bool/#default) | Returns the property value as bool. |
|[ to_byte_array()](./to_byte_array/#default) | Returns the property value as byte array. |
|[ to_date_time()](./to_date_time/#default) | Returns the property value as DateTime in UTC. |
|[ to_double()](./to_double/#default) | Returns the property value as double. |
|[ to_int()](./to_int/#default) | Returns the property value as integer. |

### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(MY_DIR + "Properties.docx")

# The "Document" object contains some of its metadata in its members.
print(f"Document filename:\n\t \"{doc.original_file_name}\"")

# The document also stores metadata in its built-in properties.
# Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
print("Built-in Properties:")
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f"\tType:\t{doc_property.type}")

    # Some properties may store multiple values.
    if isinstance(doc_property.value, list):
        for value in doc_property.value:
            print(f"\tValue:\t\"{value}\"")
    else:
        print(f"\tValue:\t\"{doc_property.value}\"")
```

### See Also

* module [aspose.words.properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)

