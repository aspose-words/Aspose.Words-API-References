---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection classe"
linktitle: "BaseWebExtensionCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection classe. Classe base per le collezioni TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection e WebExtensionReferenceCollection. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Classe base per le collezioni [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) e [WebExtensionReferenceCollection](../webextensionreferencecollection/). Per saperne di più, visita l'articolo della documentazione [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parametro | Descrizione |
| --- | --- |
| T | Tipo di un elemento della collezione. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(T) | Aggiunge l'elemento specificato alla collezione. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un enumeratore che può iterare attraverso una collezione. |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta un elemento all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, T) | Ottiene o imposta un elemento all'indice specificato. |
| [Remove](./remove/)(int32_t) | Rimuove l'elemento all'indice specificato dalla collezione. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Esempi



Mostra come lavorare con la collezione di estensioni web di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Stampa tutte le proprietà dell'estensione web del documento.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Rimuovi l'estensione web.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
