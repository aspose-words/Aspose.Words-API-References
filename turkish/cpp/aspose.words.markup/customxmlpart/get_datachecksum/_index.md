---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum yöntemi"
linktitle: "get_DataChecksum"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum yöntemi. C++'ta Data içeriğinin döngüsel artıklık kontrolü (CRC) sağlama toplamını belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


[Data](../get_data/) içeriğinin döngüsel artıklık kontrolü (CRC) sağlama toplamını belirtir.

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Örnekler



Çalışma zamanında sağlama toplamının nasıl hesaplandığını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// Sağlama toplamı yalnızca okunur ve ilgili özel XML veri bölümünün verileri kullanılarak hesaplanır.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Etiketin XmlPart'ını değiştirdik ve sağlama toplamı çalışma zamanında güncellendi.
ASSERT_NE(checksum, updatedChecksum);
```

## Ayrıca Bakınız

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
