---
title: XmlMapping.is_mapped property
linktitle: is_mapped property
articleTitle: is_mapped property
second_title: Aspose.Words for Python
description: "XmlMapping.is_mapped property. Returns ``True`` if the parent structured document tag is successfully mapped to XML data."
type: docs
weight: 20
url: /ru/python-net/aspose.words.markup/xmlmapping/is_mapped/
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
# Создать часть XML, содержащую текст, и добавить её в коллекцию CustomXmlPart документа.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# Создать структурированный тег документа, который будет отображать содержимое нашего CustomXmlPart.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
# Установить сопоставление для нашего структурированного тега документа. Это сопоставление будет указывать
# нашему структурированному тегу документа отображать часть текстового содержимого части XML, на которую указывает XPath.
# В этом случае это будет содержимое второго элемента "<text>" первого элемента "<root>": "Text element #2".
tag.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', "xmlns:ns='http://www.w3.org/2001/XMLSchema'")
self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual('/root[1]/text[2]', tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)
# Добавьте структурированный тег документа в документ, чтобы отобразить содержимое из нашей пользовательской части.
doc.first_section.body.append_child(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.XmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

