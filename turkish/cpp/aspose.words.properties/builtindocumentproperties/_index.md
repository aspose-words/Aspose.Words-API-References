---
title: "Aspose::Words::Properties::BuiltInDocumentProperties class"
linktitle: "BuiltInDocumentProperties"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::BuiltInDocumentProperties sınıfı. Yerleşik belge özelliklerinin bir koleksiyonu. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.properties/builtindocumentproperties/
---
## BuiltInDocumentProperties class


Yerleşik belge özelliklerinin bir koleksiyonu. Daha fazla bilgi edinmek için [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/) dokümantasyon makalesini ziyaret edin.

```cpp
class BuiltInDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clear](../documentpropertycollection/clear/)() | Koleksiyondaki tüm özellikleri kaldırır. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Koleksiyonda belirtilen ada sahip bir özellik varsa **true** döndürür. |
| [get_Author](./get_author/)() | Belgenin yazarının adını alır veya ayarlar. |
| [get_Bytes](./get_bytes/)() | Belgedeki bayt sayısının bir tahminini temsil eder. |
| [get_Category](./get_category/)() | Belgenin kategorisini alır veya ayarlar. |
| [get_Characters](./get_characters/)() | Belgedeki karakter sayısının bir tahminini temsil eder. |
| [get_CharactersWithSpaces](./get_characterswithspaces/)() | Belgedeki karakter (boşluklar dahil) sayısının bir tahminini temsil eder. |
| [get_Comments](./get_comments/)() | Belge yorumlarını alır veya ayarlar. |
| [get_Company](./get_company/)() | Şirket özelliğini alır veya ayarlar. |
| [get_ContentStatus](./get_contentstatus/)() | Belgenin içerik durumunu alır. |
| [get_ContentType](./get_contenttype/)() | Belgenin içerik türünü alır. |
| [get_Count](../documentpropertycollection/get_count/)() | Koleksiyondaki öğe sayısını alır. |
| [get_CreatedTime](./get_createdtime/)() | Belgenin oluşturulma tarihini UTC olarak alır veya ayarlar. |
| [get_HeadingPairs](./get_headingpairs/)() | Belge başlıklarını ve bunların adlarını belirtir. |
| [get_HyperlinkBase](./get_hyperlinkbase/)() | Bu belgede göreceli bağlantıların değerlendirilmesinde kullanılan temel dizeyi belirtir. |
| [get_HyperlinksChanged](./get_hyperlinkschanged/)() | Bir belgedeki bağlantıların değişip değişmediğini gösterir. |
| [get_Keywords](./get_keywords/)() | Belge anahtar kelimelerini alır veya ayarlar. |
| [get_LastPrinted](./get_lastprinted/)() | Belgenin son yazdırılma tarihini UTC olarak alır veya ayarlar. |
| [get_LastSavedBy](./get_lastsavedby/)() | Son yazarın adını alır veya ayarlar. |
| [get_LastSavedTime](./get_lastsavedtime/)() | Son kaydetme zamanını UTC olarak alır veya ayarlar. |
| [get_Lines](./get_lines/)() | Belgedeki satır sayısının tahmini bir değerini temsil eder. |
| [get_LinksUpToDate](./get_linksuptodate/)() | Bir belgedeki bağlantıların güncel olup olmadığını gösterir. |
| [get_Manager](./get_manager/)() | Yönetici özelliğini alır veya ayarlar. |
| [get_NameOfApplication](./get_nameofapplication/)() | Uygulamanın adını alır veya ayarlar. |
| [get_Pages](./get_pages/)() | Belgedeki sayfa sayısının tahmini bir değerini temsil eder. |
| [get_Paragraphs](./get_paragraphs/)() | Belgedeki paragraf sayısının tahmini bir değerini temsil eder. |
| [get_RevisionNumber](./get_revisionnumber/)() | Belge revizyon numarasını alır veya ayarlar. |
| [get_ScaleCrop](./get_scalecrop/)() | Belge küçük resminin kırpılıp kırpılmadığını veya ekrana sığacak şekilde ölçeklendirilip ölçeklendirilmediğini gösterir. |
| [get_Security](./get_security/)() | Belgenin güvenlik seviyesini sayısal bir değer olarak belirtir. |
| [get_SharedDocument](./get_shareddocument/)() | Belgenin paylaşılan bir belge olup olmadığını gösterir. |
| [get_Subject](./get_subject/)() | Belgenin konusunu alır veya ayarlar. |
| [get_Template](./get_template/)() | Belge şablonunun bilgi adını alır veya ayarlar. |
| [get_Thumbnail](./get_thumbnail/)() | Belgenin küçük resmini alır veya ayarlar. |
| [get_Title](./get_title/)() | Belgenin başlığını alır veya ayarlar. |
| [get_TitlesOfParts](./get_titlesofparts/)() | Dizideki her dize, belgedeki bir parçanın adını belirtir. |
| [get_TotalEditingTime](./get_totaleditingtime/)() | Toplam düzenleme süresini dakikalar cinsinden alır veya ayarlar. |
| [get_Version](./get_version/)() | Belgeyi oluşturan uygulamanın sürüm numarasını temsil eder. |
| [get_Words](./get_words/)() | Belgedeki kelime sayısının tahmini bir değerini temsil eder. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(System::String) override | Özelliğin adıyla bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | İndeksle bir [DocumentProperty](../documentproperty/) nesnesi döndürür. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Bir özelliğin adını kullanarak indeksini alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Koleksiyondan belirtilen ada sahip bir özelliği kaldırır. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Belirtilen indeksteki bir özelliği kaldırır. |
| [set_Author](./set_author/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Author](./get_author/). |
| [set_Bytes](./set_bytes/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Bytes](./get_bytes/). |
| [set_Category](./set_category/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Category](./get_category/). |
| [set_Characters](./set_characters/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Characters](./get_characters/). |
| [set_CharactersWithSpaces](./set_characterswithspaces/)(int32_t) | Belgedeki karakter (boşluklar dahil) sayısının bir tahminini temsil eder. |
| [set_Comments](./set_comments/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Comments](./get_comments/). |
| [set_Company](./set_company/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Company](./get_company/). |
| [set_ContentStatus](./set_contentstatus/)(const System::String\&) | Belgenin içerik durumunu ayarlar. |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Belgenin içerik türünü ayarlar. |
| [set_CreatedTime](./set_createdtime/)(System::DateTime) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_CreatedTime](./get_createdtime/). |
| [set_HeadingPairs](./set_headingpairs/)(const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs](./get_headingpairs/). |
| [set_HyperlinkBase](./set_hyperlinkbase/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase](./get_hyperlinkbase/). |
| [set_Keywords](./set_keywords/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Keywords](./get_keywords/). |
| [set_LastPrinted](./set_lastprinted/)(System::DateTime) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastPrinted](./get_lastprinted/). |
| [set_LastSavedBy](./set_lastsavedby/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedBy](./get_lastsavedby/). |
| [set_LastSavedTime](./set_lastsavedtime/)(System::DateTime) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime](./get_lastsavedtime/). |
| [set_Lines](./set_lines/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Lines](./get_lines/). |
| [set_LinksUpToDate](./set_linksuptodate/)(bool) | Bir belgedeki bağlantıların güncel olup olmadığını gösterir. |
| [set_Manager](./set_manager/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Manager](./get_manager/). |
| [set_NameOfApplication](./set_nameofapplication/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_NameOfApplication](./get_nameofapplication/). |
| [set_Pages](./set_pages/)(int32_t) | Belgedeki sayfa sayısının tahmini bir değerini temsil eder. |
| [set_Paragraphs](./set_paragraphs/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Paragraphs](./get_paragraphs/). |
| [set_RevisionNumber](./set_revisionnumber/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_RevisionNumber](./get_revisionnumber/). |
| [set_Security](./set_security/)(Aspose::Words::Properties::DocumentSecurity) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Security](./get_security/). |
| [set_Subject](./set_subject/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Subject](./get_subject/). |
| [set_Template](./set_template/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Template](./get_template/). |
| [set_Thumbnail](./set_thumbnail/)(const System::ArrayPtr\<uint8_t\>\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail](./get_thumbnail/). |
| [set_Title](./set_title/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Title](./get_title/). |
| [set_TitlesOfParts](./set_titlesofparts/)(const System::ArrayPtr\<System::String\>\&) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_TitlesOfParts](./get_titlesofparts/). |
| [set_TotalEditingTime](./set_totaleditingtime/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_TotalEditingTime](./get_totaleditingtime/). |
| [set_Version](./set_version/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Version](./get_version/). |
| [set_Words](./set_words/)(int32_t) | Ayarlayıcı [Aspose::Words::Properties::BuiltInDocumentProperties::get_Words](./get_words/). |
| static [Type](./type/)() |  |
## Açıklamalar


Adlarına göre (indeksleyici kullanarak) ve uygun türde değerler döndüren bir dizi tiplenmiş özellik aracılığıyla [DocumentProperty](../documentproperty/) nesnelerine erişim sağlar.

Özellik adları büyük/küçük harfe duyarsızdır.

Koleksiyondaki özellikler ada göre alfabetik olarak sıralanır.

## Örnekler



Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// \"Document\" nesnesi, meta verilerinin bir kısmını üyelerinde tutar.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Belge ayrıca meta verileri yerleşik özelliklerinde depolar.
// Her yerleşik özellik, belgenin \"BuiltInDocumentProperties\" nesnesinin bir üyesidir.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Bazı özellikler birden fazla değer depolayabilir.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Ayrıca Bakınız

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
