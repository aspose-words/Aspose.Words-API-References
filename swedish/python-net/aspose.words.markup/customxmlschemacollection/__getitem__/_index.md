---
title: CustomXmlSchemaCollection indexer
linktitle: CustomXmlSchemaCollection indexer
articleTitle: CustomXmlSchemaCollection indexer
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection indexer. Gets or sets the element at the specified index."
type: docs
weight: 10
url: /sv/python-net/aspose.words.markup/customxmlschemacollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets or sets the element at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to work with an XML schema collection.

```python
doc = aw.Document()
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Hello, World!</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
# Lägg till en XML-schemaassociation.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Klona den anpassade XML-delens XML-schemaassociationssamling,
# och lägg sedan till ett par nya scheman i klonen.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Enumerera schemana och skriv ut varje element.
for schema in schemas:
    print(schema)
# Nedan finns tre sätt att ta bort scheman från samlingen.
# 1 - Ta bort ett schema efter index:
schemas.remove_at(2)
# 2 - Ta bort ett schema efter värde:
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 - Använd metoden "Clear" för att tömma samlingen på en gång.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

