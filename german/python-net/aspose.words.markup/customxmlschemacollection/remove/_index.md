---
title: CustomXmlSchemaCollection.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection.remove method. Removes the specified value from the collection."
type: docs
weight: 70
url: /de/python-net/aspose.words.markup/customxmlschemacollection/remove/
---

## remove(name) {#str}

Removes the specified value from the collection.


```python
def remove(self, name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | str | The case-sensitive value to remove. |

### Examples

Shows how to work with an XML schema collection.

```python
doc = aw.Document()
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Hello, World!</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
# Fügen Sie eine XML‑Schema‑Verknüpfung hinzu.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Klonen Sie die XML‑Schema‑Verknüpfungssammlung des benutzerdefinierten XML‑Teils,
# und fügen Sie dann ein paar neue Schemas zum Klon hinzu.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Durchlaufen Sie die Schemas und geben Sie jedes Element aus.
for schema in schemas:
    print(schema)
# Im Folgenden sind drei Methoden zum Entfernen von Schemas aus der Sammlung aufgeführt.
# 1 - Entfernen Sie ein Schema nach Index:
schemas.remove_at(2)
# 2 - Entfernen Sie ein Schema nach Wert:
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 - Verwenden Sie die Methode "Clear", um die Sammlung auf einmal zu leeren.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

