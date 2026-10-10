---
title: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentPropertyCollection::idx_get yöntemi. C++'ta bir indeksle DocumentProperty nesnesi döndürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


İndeksle bir [DocumentProperty](../../documentproperty/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Alınacak [DocumentProperty](../../documentproperty/) nesnesinin sıfır tabanlı indeksi. |

## Örnekler



Özel belge özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Her belge, yerleşik özellikler gibi anahtar‑değer çiftleri olan bir özel özellik koleksiyonu içerir.
// Belgenin sabit bir yerleşik özellik listesi vardır. Kullanıcı tüm özel özellikleri oluşturur.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Özelliğin adıyla bir [DocumentProperty](../../documentproperty/) nesnesi döndürür.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | System::String | Alınacak özelliğin büyük/küçük harfe duyarsız adı. |
## Açıklamalar


Belirtilen adla bir özellik bulunamazsa **null** döndürür.

## Örnekler



Tarih ve saat içeren bir özel belge özelliğinin nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Ayrıca Bakınız

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
