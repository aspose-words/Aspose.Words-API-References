---
title: "Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt metodu"
linktitle: "RemoveAt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt yöntemi. Belirtilen dizindeki bir öğeyi C++'ta kaldırır."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.markup/customxmlpartcollection/removeat/
---
## CustomXmlPartCollection::RemoveAt method


Belirtilen indeksteki bir öğeyi kaldırır.

```cpp
void Aspose::Words::Markup::CustomXmlPartCollection::RemoveAt(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Sıfır tabanlı indeks. |

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

* Class [CustomXmlPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
