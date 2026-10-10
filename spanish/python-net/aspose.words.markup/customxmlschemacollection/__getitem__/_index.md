---
title: CustomXmlSchemaCollection indexer
linktitle: CustomXmlSchemaCollection indexer
articleTitle: CustomXmlSchemaCollection indexer
second_title: Aspose.Words for Python
description: "CustomXmlSchemaCollection indexer. Gets or sets the element at the specified index."
type: docs
weight: 10
url: /es/python-net/aspose.words.markup/customxmlschemacollection/__getitem__/
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
# Agregar una asociación de esquema XML.
xml_part.schemas.add('http://www.w3.org/2001/XMLSchema')
# Clonar la colección de asociaciones de esquemas XML de la parte XML personalizada,
# y luego agregar un par de esquemas nuevos al clon.
schemas = xml_part.schemas.clone()
schemas.add('http://www.w3.org/2001/XMLSchema-instance')
schemas.add('http://schemas.microsoft.com/office/2006/metadata/contentType')
self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of('http://schemas.microsoft.com/office/2006/metadata/contentType'))
# Enumerar los esquemas e imprimir cada elemento.
for schema in schemas:
    print(schema)
# A continuación se presentan tres formas de eliminar esquemas de la colección.
# 1 -  Eliminar un esquema por índice:
schemas.remove_at(2)
# 2 -  Eliminar un esquema por valor:
schemas.remove('http://www.w3.org/2001/XMLSchema')
# 3 -  Usar el método "Clear" para vaciar la colección de una vez.
schemas.clear()
self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

