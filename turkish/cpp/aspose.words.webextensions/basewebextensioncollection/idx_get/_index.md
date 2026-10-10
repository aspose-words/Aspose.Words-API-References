---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_get metodu. Belirtilen indeksteki bir öğeyi C++'da alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.webextensions/basewebextensioncollection/idx_get/
---
## BaseWebExtensionCollection::idx_get method


Belirtilen indeksteki öğeyi alır veya ayarlar.

```cpp
T Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Öğenin sıfır tabanlı indeksi. |

## Örnekler



Bir belgenin web uzantıları koleksiyonuyla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Belgenin web uzantısının tüm özelliklerini yazdır.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Web uzantısını kaldır.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Ayrıca Bakınız

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
