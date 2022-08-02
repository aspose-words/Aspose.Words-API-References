---
title: set_mapping method
second_title: Aspose.Words for Python via .NET API Reference
description: "Sets a mapping between the parent structured document tag and an XML node of a custom XML data part."
type: docs
weight: 70
url: /python-net/aspose.words.markup/xmlmapping/set_mapping/
---

## set_mapping(custom_xml_part, x_path, prefix_mapping) {#customxmlpart_str_str}

Sets a mapping between the parent structured document tag and an XML node of a custom XML data part.


```python
def set_mapping(self, custom_xml_part: aspose.words.markup.CustomXmlPart, x_path: str, prefix_mapping: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| custom_xml_part | [CustomXmlPart](../../customxmlpart/) |  |
| x_path | str |  |
| prefix_mapping | str |  |

### Returns

A flag indicating whether the parent structured document tag is successfully mapped to
the XML node.


### Examples

Shows how to create a structured document tag with custom XML data.

```python
doc = aw.Document()

# Construct an XML part that contains data and add it to the document's collection.
# If we enable the "Developer" tab in Microsoft Word,
# we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
xml_part_id = str(uuid.uuid4())
xml_part_content = "<root><text>Hello world!</text></root>"
xml_part = doc.custom_xml_parts.add(xml_part_id, xml_part_content)

self.assertEqual(xml_part_content.encode('ascii'), xml_part.data)
self.assertEqual(xml_part_id, xml_part.id)

# Below are two ways to refer to XML parts.
# 1 -  By an index in the custom XML part collection:
self.assertEqual(xml_part, doc.custom_xml_parts[0])

# 2 -  By GUID:
self.assertEqual(xml_part, doc.custom_xml_parts.get_by_id(xml_part_id))

# Add an XML schema association.
xml_part.schemas.add("http://www.w3.org/2001/XMLSchema")

# Clone a part, and then insert it into the collection.
xml_part_clone = xml_part.clone()
xml_part_clone.id = str(uuid.uuid4())
doc.custom_xml_parts.add(xml_part_clone)

self.assertEqual(2, doc.custom_xml_parts.count)

# Iterate through the collection and print the contents of each part.
for index, part in enumerate(doc.custom_xml_parts):
    print(f"XML part index {index}, ID: {part.id}")
    print(f"\tContent: {part.data.decode('utf-8')}")

# Use the "remove_at" method to remove the cloned part by index.
doc.custom_xml_parts.remove_at(1)

self.assertEqual(1, doc.custom_xml_parts.count)

# Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
custom_xml_parts = doc.custom_xml_parts.clone()
custom_xml_parts.clear()

# Create a structured document tag that will display our part's contents and insert it into the document body.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
tag.xml_mapping.set_mapping(xml_part, "/root[1]/text[1]", "")

doc.first_section.body.append_child(tag)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.creating_custom_xml.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

