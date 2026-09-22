---
title: "Aspose::Words::Markup::XmlMapping sınıfı"
linktitle: "XmlMapping"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::XmlMapping sınıfı. Belgenin içinde bir özel XML veri bölümünde depolanan bir XML öğesi ile üst yapılandırılmış belge etiketi arasında bir eşleme oluşturmak için kullanılan bilgileri belirtir. Daha fazla bilgi edinmek için C++'daki  dokümantasyon makalesini ziyaret edin."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Belgedeki bir özel XML veri bölümünde depolanan bir XML öğesi ile üst yapılandırılmış belge etiketi arasında bir eşleme oluşturmak için kullanılan bilgileri belirtir. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class XmlMapping : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Delete](./delete/)() | Üst yapılandırılmış belgenin XML verisine eşlemesini siler. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Üst yapılandırılmış belge etiketinin eşlendiği özel XML veri bölümünü döndürür. |
| [get_IsMapped](./get_ismapped/)() | Üst yapılandırılmış belge etiketi XML verisine başarıyla eşlendiğinde **true** döndürür. |
| [get_PrefixMappings](./get_prefixmappings/)() const | XPath'i değerlendirmek için XML ad alanı önek eşlemelerini döndürür. [XPath](./get_xpath/). |
| [get_StoreItemId](./get_storeitemid/)() | XPath ifadesini değerlendirmek için kullanılacak özel XML veri bölümünün özel XML veri tanımlayıcısını belirtir. [XPath](./get_xpath/) ifadesi. |
| [get_XPath](./get_xpath/)() const | Üst yapılandırılmış belge etiketine eşlenen özel XML düğümünü bulmak için değerlendirilen XPath ifadesini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Üst yapılandırılmış belge etiketi ile bir özel XML veri bölümünün XML düğümü arasında bir eşleme ayarlar. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
