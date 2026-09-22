---
title: "Aspose::Words::Markup::CustomPart::get_IsExternal yöntemi."
linktitle: "get_IsExternal"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomPart::get_IsExternal yöntemi. Bu özel parça OOXML paketinin içinde depolanıyorsa false. Bu özel parça harici bir hedefse true. C++'ta."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.markup/custompart/get_isexternal/
---
## CustomPart::get_IsExternal method


Bu özel bölüm OOXML paketinin içinde depolanıyorsa False, dış bir hedefse True.

```cpp
bool Aspose::Words::Markup::CustomPart::get_IsExternal() const
```

## Açıklamalar


Varsayılan değer **false**'tur.

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

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
