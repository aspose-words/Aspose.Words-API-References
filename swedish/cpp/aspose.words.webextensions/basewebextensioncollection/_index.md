---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection klass"
linktitle: "BaseWebExtensionCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection-klass. Basklass för TaskPaneCollection-, WebExtensionBindingCollection-, WebExtensionPropertyCollection- och WebExtensionReferenceCollection-samlingar. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Basklass för [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) och [WebExtensionReferenceCollection](../webextensionreferencecollection/) samlingar. För att lära dig mer, besök dokumentationsartikeln [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parameter | Beskrivning |
| --- | --- |
| T | Typ av ett samlingsobjekt. |
## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(T) | Lägger till angivet objekt i samlingen. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar en enumerator som kan iterera genom en samling. |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller anger ett objekt på det angivna indexet. |
| [idx_set](./idx_set/)(int32_t, T) | Hämtar eller anger ett objekt på det angivna indexet. |
| [Remove](./remove/)(int32_t) | Tar bort objektet på det angivna indexet från samlingen. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beskrivning |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Exempel



Visar hur man arbetar med ett dokuments samling av webbutökningar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Skriv ut alla egenskaper för dokumentets webbutökning.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Ta bort webbutökningen.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Se även

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
