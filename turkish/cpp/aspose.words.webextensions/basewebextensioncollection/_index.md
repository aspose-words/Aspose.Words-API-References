---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection sınıfı"
linktitle: "BaseWebExtensionCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection sınıfı. TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection ve WebExtensionReferenceCollection koleksiyonları için temel sınıftır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


[TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) ve [WebExtensionReferenceCollection](../webextensionreferencecollection/) koleksiyonları için temel sınıf. Daha fazla bilgi için [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/) belge makalesini ziyaret edin.

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parametre | Açıklama |
| --- | --- |
| T | Bir koleksiyon öğesinin türü. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(T) | Belirtilen öğeyi koleksiyona ekler. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Bir koleksiyon içinde yineleme yapabilen bir enumerator döndürür. |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, T) | Belirtilen indeksteki öğeyi alır veya ayarlar. |
| [Remove](./remove/)(int32_t) | Belirtilen indeksteki öğeyi koleksiyondan kaldırır. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
