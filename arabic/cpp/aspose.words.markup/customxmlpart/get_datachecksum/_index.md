---
title: "طريقة Aspose::Words::Markup::CustomXmlPart::get_DataChecksum"
linktitle: "get_DataChecksum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::CustomXmlPart::get_DataChecksum. تحدد قيمة فحص التكرار الدوري (CRC) لمحتوى Data في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.markup/customxmlpart/get_datachecksum/
---
## CustomXmlPart::get_DataChecksum method


تحدد قيمة فحص التكرار الدوري (CRC) لمحتوى [Data](../get_data/).

```cpp
int64_t Aspose::Words::Markup::CustomXmlPart::get_DataChecksum()
```


## أمثلة



يظهر كيف يتم حساب قيمة الفحص أثناء وقت التشغيل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto richText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(richText);

// قيمة الفحص للقراءة فقط ويتم حسابها باستخدام بيانات الجزء المخصص من XML المقابل.
richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>ContentControl</text></root>"), u"/root/text", u"");

int64_t checksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << checksum << std::endl;

richText->get_XmlMapping()->SetMapping(doc->get_CustomXmlParts()->Add(System::ObjectExt::ToString(System::Guid::NewGuid()), u"<root><text>Updated ContentControl</text></root>"), u"/root/text", u"");

int64_t updatedChecksum = richText->get_XmlMapping()->get_CustomXmlPart()->get_DataChecksum();
std::cout << updatedChecksum << std::endl;

// قمنا بتغيير XmlPart للعلامة، وتم تحديث قيمة الفحص أثناء وقت التشغيل.
ASSERT_NE(checksum, updatedChecksum);
```

## انظر أيضًا

* Class [CustomXmlPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
