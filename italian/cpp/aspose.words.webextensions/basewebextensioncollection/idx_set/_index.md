---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set metodo"
linktitle: "idx_set"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set metodo. Ottiene o imposta un elemento all'indice specificato in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.webextensions/basewebextensioncollection/idx_set/
---
## BaseWebExtensionCollection::idx_set method


Ottiene o imposta un elemento all'indice specificato.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::idx_set(int32_t index, T value)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Indice basato su zero dell'elemento. |

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

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
