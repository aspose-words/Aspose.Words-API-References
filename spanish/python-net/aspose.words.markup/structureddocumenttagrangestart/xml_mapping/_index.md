---
title: StructuredDocumentTagRangeStart.xml_mapping property
linktitle: xml_mapping property
articleTitle: xml_mapping property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.xml_mapping property. Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document."
type: docs
weight: 190
url: /es/python-net/aspose.words.markup/structureddocumenttagrangestart/xml_mapping/
---

## StructuredDocumentTagRangeStart.xml_mapping property

Gets an object that represents the mapping of this structured document tag range to XML data
in a custom XML part of the current document.


```python
@property
def xml_mapping(self) -> aspose.words.markup.XmlMapping:
    ...

```

### Remarks

You can use the [XmlMapping.set_mapping()](../../xmlmapping/set_mapping/#customxmlpart_str_str) method of this
object to map a structured document tag range to XML data.



### Examples

Shows how to set XML mappings for the range start of a structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Multi-section structured document tags.docx')
# Construir una parte XML que contenga texto y agregarla a la colección CustomXmlPart del documento.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# Cree una etiqueta de documento estructurado que mostrará el contenido de nuestro CustomXmlPart en el documento.
sdt_range_start = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, True).as_structured_document_tag_range_start()
# Si establecemos una asignación para nuestra etiqueta de documento estructurado,
# solo mostrará una parte del CustomXmlPart al que apunta el XPath.
# Este XPath apuntará al segundo elemento "<text>" del contenido del primer elemento "<root>" de nuestro CustomXmlPart.
sdt_range_start.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', None)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

