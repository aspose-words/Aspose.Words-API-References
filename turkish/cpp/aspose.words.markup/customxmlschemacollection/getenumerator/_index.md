---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::GetEnumerator yöntemi"
linktitle: "GetEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::GetEnumerator yöntemi. Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür C++'da."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.markup/customxmlschemacollection/getenumerator/
---
## CustomXmlSchemaCollection::GetEnumerator method


Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> Aspose::Words::Markup::CustomXmlSchemaCollection::GetEnumerator() override
```


## Örnekler



Bir XML şema koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Bir XML şema ilişkilendirmesi ekleyin.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Özel XML bölümünün XML şema ilişkilendirme koleksiyonunu klonlayın,
// ve ardından klona birkaç yeni şema ekleyin.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Şemaları sıralayın ve her öğeyi yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Aşağıda koleksiyondan şema kaldırmanın üç yolu verilmiştir.
// 1 -  Şemayı indeksine göre kaldır:
schemas->RemoveAt(2);

// 2 -  Şemayı değerine göre kaldır:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  \"Clear\" yöntemini kullanarak koleksiyonu bir kerede boşaltın.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Ayrıca Bakınız

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
