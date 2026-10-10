---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set méthode"
linktitle: "idx_set"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set méthode. Obtient ou définit un élément à l'index spécifié en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.webextensions/basewebextensioncollection/idx_set/
---
## BaseWebExtensionCollection::idx_set method


Obtient ou définit un élément à l'index spécifié.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::idx_set(int32_t index, T value)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Index de l'élément basé sur zéro. |

## Exemples



Montre comment travailler avec la collection d'extensions Web d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Imprime toutes les propriétés de l'extension Web du document.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Supprimez l'extension web.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Voir aussi

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
