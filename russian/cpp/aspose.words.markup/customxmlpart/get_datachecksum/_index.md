---
title: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum метод"
linktitle: "get_DataChecksum"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomXmlPart::get_DataChecksum метод. Указывает контрольную сумму CRC (циклический избыточный код) содержимого Data в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


Указывает контрольную сумму CRC (циклический избыточный код) содержимого [Data](../get_data/).

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## Примеры



Показывает, как вычисляется контрольная сумма во время выполнения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// Контрольная сумма только для чтения и вычисляется с использованием данных соответствующей пользовательской XML‑части.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// Мы изменили XmlPart тега, и контрольная сумма была обновлена во время выполнения.
ASSERT_NE(checksum, updatedChecksum);
```

## См. также

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
