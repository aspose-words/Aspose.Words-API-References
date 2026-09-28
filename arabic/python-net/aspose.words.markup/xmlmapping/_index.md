---
title: XmlMapping class
linktitle: XmlMapping class
articleTitle: XmlMapping class
second_title: Aspose.Words for Python
description: "aspose.words.markup.XmlMapping class. Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document"
type: docs
weight: 210
url: /ar/python-net/aspose.words.markup/xmlmapping/
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
# أنشئ جزء XML يحتوي على نص وأضفه إلى مجموعة CustomXmlPart في المستند.
xml_part_id = '{' + str(uuid.uuid4()) + '}'
xml_part_content = '<root><text>Text element #1</text><text>Text element #2</text></root>'
xml_part = doc.custom_xml_parts.add(id=xml_part_id, xml=xml_part_content)
self.assertEqual('<root><text>Text element #1</text><text>Text element #2</text></root>', system_helper.text.Encoding.get_string(xml_part.data, system_helper.text.Encoding.utf_8()))
# أنشئ علامة مستند مهيكلة ستعرض محتويات CustomXmlPart الخاص بنا.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
# عيّن تخطيطًا لعلامة المستند المهيكلة الخاصة بنا. سيقوم هذا التخطيط بإرشاد
# علامة المستند المهيكلة الخاصة بنا لعرض جزء من محتوى نص جزء XML الذي يشير إليه XPath.
# في هذه الحالة، سيكون المحتوى هو العنصر الثاني "<text>" من العنصر الأول "<root>": "Text element #2".
tag.xml_mapping.set_mapping(xml_part, '/root[1]/text[2]', "xmlns:ns='http://www.w3.org/2001/XMLSchema'")
self.assertTrue(tag.xml_mapping.is_mapped)
self.assertEqual(xml_part, tag.xml_mapping.custom_xml_part)
self.assertEqual('/root[1]/text[2]', tag.xml_mapping.xpath)
self.assertEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.xml_mapping.prefix_mappings)
# أضف علامة المستند المهيكلة إلى المستند لعرض المحتوى من الجزء المخصص الخاص بنا.
doc.first_section.body.append_child(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.XmlMapping.docx')
```

### See Also

* module [aspose.words.markup](../)

