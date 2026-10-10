---
title: "Aspose::Words::Markup::XmlMapping::get_IsMapped metodu"
linktitle: "get_IsMapped"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::XmlMapping::get_IsMapped metodu. C++'ta üst yapı belge etiketinin XML verisine başarıyla eşlendiği durumda true döndürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.markup/xmlmapping/get_ismapped/
---
## XmlMapping::get_IsMapped method


Üst yapılandırılmış belge etiketi XML verisine başarıyla eşlendiğinde **true** döndürür.

```cpp
bool Aspose::Words::Markup::XmlMapping::get_IsMapped()
```


## Örnekler



Özel XML bölümleri için XML eşlemelerinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Metin içeren bir XML bölümü oluşturun ve belgenin CustomXmlPart koleksiyonuna ekleyin.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// CustomXmlPart'ımızın içeriğini gösterecek bir yapılandırılmış belge etiketi oluşturun.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Yapılandırılmış belge etiketimiz için bir eşleme ayarlayın. Bu eşleme şu şekilde yönlendirecek
// yapılandırılmış belge etiketimizi, XPath'in işaret ettiği XML bölümünün metin içeriğinin bir kısmını görüntüleyecek şekilde.
// Bu durumda, ilk "<root>" öğesinin ikinci "<text>" öğesinin içeriği: "Text element #2" olacaktır.
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Özel bölümümüzden gelen içeriği göstermek için yapılandırılmış belge etiketini belgeye ekleyin.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Ayrıca Bakınız

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
