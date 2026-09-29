---
title: CustomXmlSchemaCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /it/python-net/aspose.words.markup/customxmlschemacollection/count/
---

## CustomXmlSchemaCollection.count property

Gets the number of elements contained in the collection.


```python
@property
def count(self) -> int:
    ...

```

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

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

