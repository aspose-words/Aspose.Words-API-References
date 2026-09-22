---
title: "Aspose::Words::Markup::CustomPart sınıfı"
linktitle: "CustomPart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomPart sınıfı. ISO/IEC 29500 standardı tarafından tanımlanmamış bir özel (keyfi içerik) bölümü temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.markup/custompart/
---
## CustomPart class


ISO/IEC 29500 standardı tarafından tanımlanmamış özel (keyfi içerik) bir bölümü temsil eder. Daha fazla bilgi edinmek için [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) dokümantasyon makalesini ziyaret edin.

```cpp
class CustomPart : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Clone](./clone/)() | Nesnenin "yeterince derin" bir kopyasını oluşturur. [Data](./get_data/) değerinin baytlarını çoğaltmaz. |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Bu özel bölümün içerik türünü belirtir. |
| [get_Data](./get_data/)() const | Bu özel bölümün verilerini içerir. |
| [get_IsExternal](./get_isexternal/)() const | Bu özel bölüm OOXML paketinin içinde depolanıyorsa False, dış bir hedefse True. |
| [get_Name](./get_name/)() const | Bu bölümün OOXML paketi içindeki mutlak adını veya hedef URL'sini alır veya ayarlar. |
| [get_RelationshipType](./get_relationshiptype/)() const | Ebeveyn bölümden bu özel bölüme olan ilişki tipini alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Ayarlayıcı, [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/) için. |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Ayarlayıcı, [Aspose::Words::Markup::CustomPart::get_Data](./get_data/) için. |
| [set_IsExternal](./set_isexternal/)(bool) | Ayarlayıcı, [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/) için. |
| [set_Name](./set_name/)(const System::String\&) | Ayarlayıcı, [Aspose::Words::Markup::CustomPart::get_Name](./get_name/) için. |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Ayarlayıcı, [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/) için. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıf, bir "unknown relationship" hedefi olan bir OOXML bölümünü temsil eder. ISO/IEC 29500 içinde tanımlanmamış tüm ilişkiler "unknown relationships" olarak kabul edilir. Bilinmeyen ilişkiler, ilişki işaretleme yönergelerine uygun olduğu sürece Office Open XML belgesinde izin verilir.

Microsoft Word, açma/kaydetme döngüleri sırasında özel bölümleri korur. Burada ek bilgi bulabilirsiniz [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx).

Aspose.Words ayrıca özel bölümleri döngü içinde işler ve ek olarak, bu bölümlere programlı olarak [CustomPart](./) ve [CustomPartCollection](../custompartcollection/) nesneleri aracılığıyla erişim sağlar.

Özel bölümleri Custom XML Data ile karıştırmayın. Custom XML Data'ya erişmeniz gerekiyorsa [CustomXmlPart](../customxmlpart/) kullanın.

## Örnekler



Bir belgenin keyfi özel bölümler koleksiyonuna nasıl erişileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// İkinci bölümü kopyalayın, ardından kopyayı koleksiyona ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Koleksiyonu döngüyle gezerek her bölümü yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Bu koleksiyondan öğeleri tek tek ya da toplu olarak kaldırabiliriz.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
