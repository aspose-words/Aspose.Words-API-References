---
title: CustomXmlSchemaCollection class
linktitle: CustomXmlSchemaCollection class
articleTitle: CustomXmlSchemaCollection class
second_title: Aspose.Words for Python
description: "aspose.words.markup.CustomXmlSchemaCollection class. A collection of strings that represent XML schemas that are associated with a custom XML part"
type: docs
weight: 70
url: /it/python-net/aspose.words.markup/customxmlschemacollection/
---

## CustomXmlSchemaCollection class

A collection of strings that represent XML schemas that are associated with a custom XML part.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Remarks

You do not create instances of this class. You access the collection of XML schemas of a custom XML part
via the [CustomXmlPart.schemas](../customxmlpart/schemas/) property.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the element at the specified index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the number of elements contained in the collection. |

### Methods

| Name | Description |
| --- | --- |
|[ add(value)](./add/#str) | Adds an item to the collection. |
|[ clear()](./clear/#default) | Removes all elements from the collection. |
|[ clone()](./clone/#default) | Makes a deep clone of this object. |
|[ index_of(value)](./index_of/#str) | Returns the zero-based index of the specified value in the collection. |
|[ remove(name)](./remove/#str) | Removes the specified value from the collection. |
|[ remove_at(index)](./remove_at/#int) | Removes a value at the specified index. |

### Examples

Shows how to work with an XML schema collection.

```python
doc = aw.Document()
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Hello, World!</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
# Aggiungi un'associazione di schema XML.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Clona la raccolta di associazioni di schema XML della parte XML personalizzata,
# e poi aggiungi un paio di nuovi schemi al clone.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Enumera gli schemi e stampa ogni elemento.
for schema in schemas:
    print(schema)
# Di seguito sono tre modi per rimuovere gli schemi dalla raccolta.
# 1 - Rimuovi uno schema per indice:
schemas.remove_at(2)
# 2 - Rimuovi uno schema per valore:
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 - Usa il metodo "Clear" per svuotare la raccolta in una volta.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../)
* class [CustomXmlPart](../customxmlpart/)
* property [CustomXmlPart.schemas](../customxmlpart/schemas/)

