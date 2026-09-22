---
title: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count metodu"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count yöntemi. Koleksiyondaki öğe sayısını C++'ta alır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


Koleksiyondaki öğe sayısını alır.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


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

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
