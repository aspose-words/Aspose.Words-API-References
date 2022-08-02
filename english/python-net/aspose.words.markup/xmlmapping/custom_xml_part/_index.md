---
title: custom_xml_part property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns the custom XML data part to which the parent structured document tag is mapped."
type: docs
weight: 10
url: /python-net/aspose.words.markup/xmlmapping/custom_xml_part/
---

## XmlMapping.custom_xml_part property

Returns the custom XML data part to which the parent structured document tag is mapped.


### Examples

Shows how to set XML mappings for custom XML parts.

```python
doc = aw.Document()

# Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
xml_part_id = str(uuid.uuid4())
xml_part_content = "<root><text>Text element #1</text><text>Text element #2</text></root>"
xml_part = doc.custom_xml_parts.add(xml_part_id, xml_part_content)

self.assertEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", xml_part.data.decode('utf-8'))

# Create a structured document tag that will display the contents of our CustomXmlPart.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)

# Set a mapping for our structured document tag. This mapping will instruct
# our structured document tag to display a portion of the XML part's text contents that the XPath points to.
# In this case, it will be contents of the the second "<text>" element of the first "<root>" element: "Text element #2".
tag.xml_mapping.set_mapping(xml_part, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'")

self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual("/root[1]/text[2]", tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)

# Add the structured document tag to the document to display the content from our custom part.
doc.first_section.body.append_child(tag)
doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.xml_mapping.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

