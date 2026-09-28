---
title: XmlMapping.xpath property
linktitle: xpath property
articleTitle: xpath property
second_title: Aspose.Words for Python
description: "XmlMapping.xpath property. Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag."
type: docs
weight: 50
url: /fr/python-net/aspose.words.markup/xmlmapping/xpath/
---

## XmlMapping.xpath property

Returns the XPath expression, which is evaluated to find the custom XML node
that is mapped to the parent structured document tag.


```python
@property
def xpath(self) -> str:
    ...

```

### Examples

Shows how to set XML mappings for custom XML parts.

```python
doc = aw.Document()
# Construisez une partie XML contenant du texte et ajoutez‑la à la collection CustomXmlPart du document.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# Créez une balise de document structuré qui affichera le contenu de notre CustomXmlPart.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
# Définissez un mappage pour notre balise de document structuré. Ce mappage indiquera
# notre balise de document structuré pour afficher une portion du texte de la partie XML pointée par le XPath.
# Dans ce cas, il s'agira du contenu du deuxième élément "<text>" du premier élément "<root>": "Text element #2".
tag.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', "xmlns:ns='http://www.w3.org/2001/XMLSchema'")
self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual('/root[1]/text[2]', tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)
# Ajoutez la balise de document structuré au document pour afficher le contenu de notre partie personnalisée.
doc.first_section.body.append_child(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.XmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

