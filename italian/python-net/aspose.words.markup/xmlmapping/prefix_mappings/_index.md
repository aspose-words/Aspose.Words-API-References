---
title: XmlMapping.prefix_mappings property
linktitle: prefix_mappings property
articleTitle: prefix_mappings property
second_title: Aspose.Words for Python
description: "XmlMapping.prefix_mappings property. Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](../xpath/)."
type: docs
weight: 30
url: /it/python-net/aspose.words.markup/xmlmapping/prefix_mappings/
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
# Costruisci una parte XML che contiene testo e aggiungila alla collezione CustomXmlPart del documento.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# Crea un tag di documento strutturato che visualizzerà il contenuto del nostro CustomXmlPart.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
# Imposta una mappatura per il nostro tag di documento strutturato. Questa mappatura istruirà
# il nostro tag di documento strutturato a visualizzare una porzione del contenuto testuale della parte XML a cui punta l'XPath.
# In questo caso, saranno i contenuti del secondo elemento "<text>" del primo elemento "<root>": "Text element #2".
tag.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', "xmlns:ns='http://www.w3.org/2001/XMLSchema'")
self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual('/root[1]/text[2]', tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)
# Aggiungi il tag di documento strutturato al documento per visualizzare il contenuto della nostra parte personalizzata.
doc.first_section.body.append_child(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.XmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

