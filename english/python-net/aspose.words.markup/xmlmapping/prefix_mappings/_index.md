---
title: XmlMapping.prefix_mappings property
linktitle: prefix_mappings property
articleTitle: prefix_mappings property
second_title: Aspose.Words for Python
description: "XmlMapping.prefix_mappings property. Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](../xpath/)."
type: docs
weight: 30
url: /python-net/aspose.words.markup/xmlmapping/prefix_mappings/
---

## XmlMapping.prefix_mappings property

Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](../xpath/).



```python
@property
def prefix_mappings(self) -> str:
    ...

```

### Remarks

Specifies the set of prefix mappings, which shall be used to interpret the XPath expression
when the XPath expression is evaluated against the custom XML data parts in the document.


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

