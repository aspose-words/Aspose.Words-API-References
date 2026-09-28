---
title: XmlMapping.prefix_mappings property
linktitle: prefix_mappings property
articleTitle: prefix_mappings property
second_title: Aspose.Words for Python
description: "XmlMapping.prefix_mappings property. Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](../xpath/)."
type: docs
weight: 30
url: /ar/python-net/aspose.words.markup/xmlmapping/prefix_mappings/
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

* module [aspose.words.markup](../../)
* class [XmlMapping](../)

