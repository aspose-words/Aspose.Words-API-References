---
title: XmlMapping.is_mapped property
linktitle: is_mapped property
articleTitle: is_mapped property
second_title: Aspose.Words for Python
description: "XmlMapping.is_mapped property. Returns ``True`` if the parent structured document tag is successfully mapped to XML data."
type: docs
weight: 20
url: /tr/python-net/aspose.words.markup/xmlmapping/is_mapped/
---

## XmlMapping.is_mapped property

Returns ``True`` if the parent structured document tag is successfully mapped to XML data.



```python
@property
def is_mapped(self) -> bool:
    ...

```

### Examples

Shows how to set XML mappings for custom XML parts.

```python
doc = aw.Document()
# Metin içeren bir XML bölümü oluşturun ve belge'nin CustomXmlPart koleksiyonuna ekleyin.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# CustomXmlPart'ımızın içeriğini gösterecek bir yapılandırılmış belge etiketi oluşturun.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
# Yapılandırılmış belge etiketimiz için bir eşleme ayarlayın. Bu eşleme şu şekilde talimat verecek
# yapılandırılmış belge etiketimiz, XPath'in işaret ettiği XML bölümünün metin içeriğinin bir kısmını gösterecek.
# Bu durumda, ilk "<root>" öğesinin ikinci "<text>" öğesinin içeriği olacaktır: "Text element #2".
tag.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', "xmlns:ns='http://www.w3.org/2001/XMLSchema'")
self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual('/root[1]/text[2]', tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)
# Özel bölümümüzden içeriği göstermek için yapılandırılmış belge etiketini belgeye ekleyin.
doc.first_section.body.append_child(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.XmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

