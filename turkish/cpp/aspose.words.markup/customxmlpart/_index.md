---
title: "Aspose::Words::Markup::CustomXmlPart class"
linktitle: "CustomXmlPart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlPart class. Bir Özel XML Veri Depolama Bölümünü (paket içinde özel XML verisi) temsil eder. Daha fazla bilgi için C++'taki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class


Bir Özel XML Veri Depolama Bölümünü (paket içindeki özel XML verisi) temsil eder. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomXmlPart : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. [Data](./get_data/) değerinin baytlarını çoğaltmaz. |
| [CustomXmlPart](./customxmlpart/)() |  |
| [get_Data](./get_data/)() const | Bu Özel XML Veri Depolama Bölümünün XML içeriğini alır veya ayarlar. |
| [get_DataChecksum](./get_datachecksum/)() | [Data](./get_data/) içeriğinin döngüsel artıklık kontrolü (CRC) sağlama toplamını belirtir. |
| [get_Id](./get_id/)() const | Bu özel XML bölümünü bir OOXML belgesi içinde tanımlayan dizeyi alır veya ayarlar. |
| [get_Schemas](./get_schemas/)() const | Bu özel XML bölümüyle ilişkili XML şemalarının kümesini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | [Aspose::Words::Markup::CustomXmlPart::get_Data](./get_data/) için ayarlayıcı. |
| [set_Id](./set_id/)(const System::String\&) | [Aspose::Words::Markup::CustomXmlPart::get_Id](./get_id/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Bir DOCX veya DOC belgesi bir veya daha fazla Özel XML Veri Depolama bölümü içerebilir. Aspose.Words, [CustomXmlParts](../../aspose.words/document/get_customxmlparts/) koleksiyonu aracılığıyla Özel XML Verilerini oluşturmayı ve çıkarmayı korur ve sağlar.

## Örnekler



Özel XML verileriyle yapılandırılmış belge etiketi oluşturmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Veri içeren bir XML bölümü oluşturun ve belge koleksiyonuna ekleyin.
// Microsoft Word'de "Developer" sekmesini etkinleştirirsek,
// Bu koleksiyondan öğeleri "XML Mapping Pane" içinde, birkaç varsayılan öğe ile birlikte bulabiliriz.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Aşağıda XML bölümlerine başvurmanın iki yolu verilmiştir.
// 1 -  Özel XML bölüm koleksiyonunda bir indeksle:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  GUID ile:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Bir XML şema ilişkilendirmesi ekleyin.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Bir bölümü klonlayın ve ardından koleksiyona ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Koleksiyonu döngüyle gezerek her bölümün içeriğini yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Klonlanan bölümü indeksle kaldırmak için "RemoveAt" metodunu kullanın.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// XML bölüm koleksiyonunu klonlayın ve ardından tüm öğelerini bir anda kaldırmak için "Clear" metodunu kullanın.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Bölümümüzün içeriğini gösterecek bir yapılandırılmış belge etiketi oluşturun ve belge gövdesine ekleyin.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
