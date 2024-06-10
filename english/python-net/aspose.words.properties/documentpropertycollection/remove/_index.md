---
title: DocumentPropertyCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "DocumentPropertyCollection.remove method. Removes a property with the specified name from the collection."
type: docs
weight: 70
url: /python-net/aspose.words.properties/documentpropertycollection/remove/
---

## remove(name) {#str}

Removes a property with the specified name from the collection.


```python
def remove(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The case-insensitive name of the property. |

### Examples

Shows how to work with a document's custom properties.

```python
doc = aw.Document()
properties = doc.custom_document_properties
self.assertEqual(0, properties.count)
# Custom document properties are key-value pairs that we can add to the document.
properties.add('Authorized', True)
properties.add('Authorized By', 'John Doe')
properties.add('Authorized Date', datetime.now())
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

* module [aspose.words.properties](../../)
* class [DocumentPropertyCollection](../)

