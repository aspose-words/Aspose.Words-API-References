---
title: DocumentProperty class
linktitle: DocumentProperty class
articleTitle: DocumentProperty class
second_title: Aspose.Words for Python
description: "aspose.words.properties.DocumentProperty class. Represents a custom or built-in document property"
type: docs
weight: 30
url: /ru/python-net/aspose.words.properties/documentproperty/
---

## DocumentProperty class

Represents a custom or built-in document property.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/python-net/work-with-document-properties/) documentation article.




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
|[ to_date_time()](./to_date_time/#default) | Returns the property value as **DateTime** in UTC. |
|[ to_double()](./to_double/#default) | Returns the property value as double. |
|[ to_int()](./to_int/#default) | Returns the property value as integer. |

### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(file_name=MY_DIR + 'Properties.docx')
# Объект "Document" содержит часть своей метаданных в своих членах.
print(f'Document filename:\n\t "{doc.original_file_name}"')
# Документ также сохраняет метаданные во встроенных свойствах.
# Каждое встроенное свойство является членом объекта "BuiltInDocumentProperties" документа.
print('Built-in Properties:')
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f'\tType:\t{doc_property.type}')
    # Некоторые свойства могут хранить несколько значений.
    if isinstance(doc_property.value, (list, tuple)):
        for value in doc_property.value:
            print(f'\tValue:\t"{value}"')
    else:
        print(f'\tValue:\t"{doc_property.value}"')
```

### See Also

* module [aspose.words.properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)

