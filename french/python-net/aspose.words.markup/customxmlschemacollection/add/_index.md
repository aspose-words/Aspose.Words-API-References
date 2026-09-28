---
title: CustomXmlSchemaCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection.add method. Adds an item to the collection."
type: docs
weight: 30
url: /fr/python-net/aspose.words.markup/customxmlschemacollection/add/
---

## add(value) {#str}

Adds an item to the collection.


```python
def add(self, value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| value | str | The item to add. |

### Examples

Shows how to work with an XML schema collection.

```python
doc = aw.Document()
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Hello, World!</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
# Ajouter une association de schéma XML.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Cloner la collection d'associations de schémas XML de la partie XML personnalisée,
# et ajouter ensuite quelques nouveaux schémas au clone.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Énumérer les schémas et afficher chaque élément.
for schema in schemas:
    print(schema)
# Voici trois façons de supprimer des schémas de la collection.
# 1 - Supprimer un schéma par indice :
schemas.remove_at(2)
# 2 - Supprimer un schéma par valeur :
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 - Utiliser la méthode "Clear" pour vider la collection en une fois.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

