---
title: StructuredDocumentTagRangeStart.xml_mapping property
linktitle: xml_mapping property
articleTitle: xml_mapping property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.xml_mapping property. Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document."
type: docs
weight: 180
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/xml_mapping/
---

## StructuredDocumentTagRangeStart.xml_mapping property

Gets an object that represents the mapping of this structured document tag range to XML data
in a custom XML part of the current document.

You can use the [XmlMapping.set_mapping()](../../xmlmapping/set_mapping/#customxmlpart_str_str) method of this
object to map a structured document tag range to XML data.



### Examples

Shows how to set XML mappings for the range start of a structured document tag.

```python
doc = aw.Document(MY_DIR + "Multi-section structured document tags.docx")

# Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
xml_part_id = str(uuid.uuid4())
xml_part_content = "<root><text>Text element #1</text><text>Text element #2</text></root>"
xml_part = doc.custom_xml_parts.add(xml_part_id, xml_part_content)

self.assertEqual("<root><text>Text element #1</text><text>Text element #2</text></root>", xml_part.data.decode('utf-8'))

# Create a structured document tag that will display the contents of our CustomXmlPart in the document.
sdt_range_start = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, True).as_structured_document_tag_range_start()

# If we set a mapping for our structured document tag,
# it will only display a portion of the CustomXmlPart that the XPath points to.
# This XPath will point to the contents second "<text>" element of the first "<root>" element of our CustomXmlPart.
sdt_range_start.xml_mapping.set_mapping(xml_part, "/root[1]/text[2]", None)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.structured_document_tag_range_start_xml_mapping.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

