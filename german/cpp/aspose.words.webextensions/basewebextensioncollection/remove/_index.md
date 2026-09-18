---
title: "Methode Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove"
linktitle: "Remove"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Methode Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove. Entfernt das Element am angegebenen Index aus der Sammlung in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.webextensions/basewebextensioncollection/remove/
---
## BaseWebExtensionCollection::Remove method


Entfernt das Element am angegebenen Index aus der Sammlung.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::Remove(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Der nullbasierte Index des Sammlungs‑Elements. |

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

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
