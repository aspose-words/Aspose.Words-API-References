---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection Klasse"
linktitle: "BaseWebExtensionCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection Klasse. Basisklasse für die Sammlungen TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection und WebExtensionReferenceCollection. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Basisklasse für die Sammlungen [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) und [WebExtensionReferenceCollection](../webextensionreferencecollection/). Weitere Informationen finden Sie im Dokumentationsartikel [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parameter | Beschreibung |
| --- | --- |
| T | Typ eines Sammlungs-Elements. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(T) | Fügt das angegebene Element zur Sammlung hinzu. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt einen Enumerator zurück, der durch eine Sammlung iterieren kann. |
| [idx_get](./idx_get/)(int32_t) | Liest ein Element am angegebenen Index aus oder setzt es. |
| [idx_set](./idx_set/)(int32_t, T) | Liest ein Element am angegebenen Index aus oder setzt es. |
| [Remove](./remove/)(int32_t) | Entfernt das Element am angegebenen Index aus der Sammlung. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Beispiele



Zeigt, wie man mit der Sammlung von Web-Extensions eines Dokuments arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Gibt alle Eigenschaften der Web-Extension des Dokuments aus.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Entferne die Web-Extension.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
