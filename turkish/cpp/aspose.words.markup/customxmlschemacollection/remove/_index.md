---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::Remove metodu"
linktitle: "Remove"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::Remove metodu. C++'ta belirtilen değeri koleksiyondan kaldırır."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.markup/customxmlschemacollection/remove/
---
## CustomXmlSchemaCollection::Remove method


Belirtilen değeri koleksiyondan kaldırır.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::Remove(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Kaldırılacak büyük/küçük harf duyarlı değer. |

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
