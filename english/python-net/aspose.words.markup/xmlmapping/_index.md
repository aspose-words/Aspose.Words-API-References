---
title: XmlMapping class
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document"
type: docs
weight: 210
url: /python-net/aspose.words.markup/xmlmapping/
---

## XmlMapping class

Specifies the information that is used to establish a mapping between the parent
structured document tag and an XML element stored within a custom XML data part in the document.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [custom_xml_part](./custom_xml_part/) | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [is_mapped](./is_mapped/) | Returns ``True`` if the parent structured document tag is successfully mapped to XML data. |
| [prefix_mappings](./prefix_mappings/) | Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](./xpath/). |
| [store_item_id](./store_item_id/) | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XmlMapping.xpath](./xpath/) expression. |
| [xpath](./xpath/) | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |

### Methods

| Name | Description |
| --- | --- |
|[ delete()](./delete/#default) | Deletes mapping of the parent structured document to XML data. |
|[ set_mapping(custom_xml_part, x_path, prefix_mapping)](./set_mapping/#customxmlpart_str_str) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |

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

* module [aspose.words.markup](../)

