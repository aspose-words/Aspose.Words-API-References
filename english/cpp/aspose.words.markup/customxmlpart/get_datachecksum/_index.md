---
title: get_DataChecksum
second_title: Aspose.Words for C++ API Reference
description: Specifies a cyclic redundancy check (CRC) checksum of the Data content.
type: docs
weight: 53
url: /cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Specifies a cyclic redundancy check (CRC) checksum of the [Data](../get_data/) content.

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Examples



Shows how the checksum is calculated in a runtime. 
```cpp
auto doc = MakeObject<Document>();

auto richText = MakeObject<StructuredDocumentTag>(doc, SdtType::RichText, MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild(richText);

// The checksum is read-only and computed using the data of the corresponding custom XML data part.
richText->get_XmlMapping()->SetMapping(
    doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text",
    u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(
    doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"),
    u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// We changed the XmlPart of the tag, and the checksum was updated at runtime.
ASSERT_NE(checksum, updatedChecksum);
```

## See Also

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words](../../../)
