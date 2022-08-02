---
title: CustomXmlSchemaCollection indexer
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the element at the specified index."
type: docs
weight: 10
url: /python-net/aspose.words.markup/customxmlschemacollection/__getitem__/
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

xml_part_id = str(uuid.uuid4())
xml_part_content = "<root><text>Hello, World!</text></root>"
xml_part = doc.custom_xml_parts.add(xml_part_id, xml_part_content)

# Add an XML schema association.
xml_part.schemas.add("http://www.w3.org/2001/XMLSchema")

# Clone the custom XML part's XML schema association collection,
# and then add a couple of new schemas to the clone.
schemas = xml_part.schemas.clone()
schemas.add("http://www.w3.org/2001/XMLSchema-instance")
schemas.add("http://schemas.microsoft.com/office/2006/metadata/contentType")

self.assertEqual(3, schemas.count)
self.assertEqual(2, schemas.index_of("http://schemas.microsoft.com/office/2006/metadata/contentType"))

# Enumerate the schemas and print each element.
for schema in schemas:
    print(schema)

# Below are three ways of removing schemas from the collection.
# 1 -  Remove a schema by index:
schemas.remove_at(2)

# 2 -  Remove a schema by value:
schemas.remove("http://www.w3.org/2001/XMLSchema")

# 3 -  Use the "clear" method to empty the collection at once.
schemas.clear()

self.assertEqual(0, schemas.count)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlSchemaCollection](../)

