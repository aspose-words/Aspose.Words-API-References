---
title: CustomXmlPart.data_checksum property
linktitle: data_checksum property
articleTitle: data_checksum property
second_title: Aspose.Words for Python
description: "CustomXmlPart.data_checksum property. Specifies a cyclic redundancy check (CRC) checksum of the [CustomXmlPart.data](../data/) content."
type: docs
weight: 30
url: /ar/python-net/aspose.words.markup/customxmlpart/data_checksum/
---

## CustomXmlPart.data_checksum property

Specifies a cyclic redundancy check (CRC) checksum of the [CustomXmlPart.data](../data/) content.



```python
@property
def data_checksum(self) -> int:
    ...

```

### Examples

Shows how the checksum is calculated in a runtime.

```python
doc = aw.Document()
rich_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.RICH_TEXT, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(rich_text)
# المجموع الاختباري هو للقراءة فقط ويتم حسابه باستخدام بيانات جزء XML المخصص المقابل.
rich_text.xml_mapping.set_mapping(doc.custom_xml_parts.add(id=str(uuid.uuid4()), xml='<root><text>ContentControl</text></root>'), '/root/text', '')
checksum = rich_text.xml_mapping.custom_xml_part.data_checksum
print(checksum)
rich_text.xml_mapping.set_mapping(doc.custom_xml_parts.add(id=str(uuid.uuid4()), xml='<root><text>Updated ContentControl</text></root>'), '/root/text', '')
updated_checksum = rich_text.xml_mapping.custom_xml_part.data_checksum
print(updated_checksum)
# قمنا بتغيير XmlPart للعلامة، وتم تحديث المجموع الاختباري أثناء التشغيل.
self.assertNotEqual(checksum, updated_checksum)
```

### See Also

* module [aspose.words.markup](../../)
* class [CustomXmlPart](../)

