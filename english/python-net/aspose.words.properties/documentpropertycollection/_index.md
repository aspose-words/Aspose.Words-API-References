---
title: DocumentPropertyCollection class
linktitle: DocumentPropertyCollection class
articleTitle: DocumentPropertyCollection class
second_title: Aspose.Words for Python
description: "aspose.words.properties.DocumentPropertyCollection class. Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections"
type: docs
weight: 40
url: /python-net/aspose.words.properties/documentpropertycollection/
---

## DocumentPropertyCollection class

Base class for [BuiltInDocumentProperties](../builtindocumentproperties/) and [CustomDocumentProperties](../customdocumentproperties/) collections.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/python-net/work-with-document-properties/) documentation article.




### Remarks

The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Returns a [DocumentProperty](../documentproperty/) object by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets number of items in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](./clear/#default) | Removes all properties from the collection. |
|[ contains(name)](./contains/#str) | Returns ``True`` if a property with the specified name exists in the collection. |
|[ get_by_name(name)](./get_by_name/#str) | Returns a [DocumentProperty](../documentproperty/) object by the name of the property. |
|[ index_of(name)](./index_of/#str) | Gets the index of a property by name. |
|[ remove(name)](./remove/#str) | Removes a property with the specified name from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a property at the specified index. |

### Examples

Shows how to work with a document's custom properties.

```python
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# Custom document properties are key-value pairs that we can add to the document.
properties.add('Authorized', True)
properties.add('Authorized By', 'John Doe')
properties.add('Authorized Date', datetime.datetime.now())
properties.add('Authorized Revision', doc.built_in_document_properties.revision_number)
properties.add('Authorized Amount', 123.45)
# The collection sorts the custom properties in alphabetic order.
self.assertEqual(1, properties.index_of('Authorized Amount'))
self.assertEqual(5, properties.count)
# Print every custom property in the document.
for prop in properties:
    print(f'Name: "{prop.name}"\n\tType: "{prop.type}"\n\tValue: "{prop.value}"')
# Display the value of a custom property using a DOCPROPERTY field.
builder = aw.DocumentBuilder(doc)
field = builder.insert_field(' DOCPROPERTY "Authorized By"').as_field_doc_property()
field.update()
self.assertEqual('John Doe', field.result)
# We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.save(ARTIFACTS_DIR + 'DocumentProperties.document_property_collection.docx')
# Below are three ways or removing custom properties from a document.
# 1 -  Remove by index:
properties.remove_at(1)
self.assertFalse(properties.contains('Authorized Amount'))
self.assertEqual(4, properties.count)
# 2 -  Remove by name:
properties.remove('Authorized Revision')
self.assertFalse(properties.contains('Authorized Revision'))
self.assertEqual(3, properties.count)
# 3 -  Empty the entire collection at once:
properties.clear()
self.assertEqual(0, properties.count)
```

### See Also

* module [aspose.words.properties](../)
* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)

