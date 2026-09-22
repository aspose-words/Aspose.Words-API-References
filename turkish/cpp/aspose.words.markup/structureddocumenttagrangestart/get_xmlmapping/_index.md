---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping method"
linktitle: "get_XmlMapping"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping metodu. Bu yapılandırılmış belge etiketi aralığının, geçerli belgenin özel bir XML bölümündeki XML verilerine eşlemesini temsil eden bir nesneyi C++'ta alır."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Bu yapılandırılmış belge etiketi aralığının mevcut belgenin özel bir XML bölümündeki XML verilerine eşlenmesini temsil eden bir nesneyi alır.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Örnekler



Yapılandırılmış bir belge etiketinin aralık başlangıcı için XML eşlemelerini nasıl ayarlayacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Metin içeren bir XML bölümü oluşturun ve belgenin CustomXmlPart koleksiyonuna ekleyin.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Belgedeki CustomXmlPart içeriğini gösterecek bir yapılandırılmış belge etiketi oluşturun.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlarsak,
// XPath'in işaret ettiği CustomXmlPart'in yalnızca bir bölümünü gösterecektir.
// Bu XPath, CustomXmlPart'imizdeki ilk "<root>" öğesinin ikinci "<text>" öğesinin içeriğine işaret edecektir.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Ayrıca Bakınız

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
