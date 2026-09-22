---
title: "Aspose::Words::Markup::CustomPartCollection::GetEnumerator yöntemi"
linktitle: "GetEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomPartCollection::GetEnumerator yöntemi. C++'ta koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumerator nesnesi döndürür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.markup/custompartcollection/getenumerator/
---
## CustomPartCollection::GetEnumerator method


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> Aspose::Words::Markup::CustomPartCollection::GetEnumerator() override
```


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

* Class [CustomPart](../../custompart/)
* Class [CustomPartCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
