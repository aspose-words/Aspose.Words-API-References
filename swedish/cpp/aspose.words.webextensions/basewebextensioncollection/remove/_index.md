---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove method"
linktitle: "Ta bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove‑metoden. Tar bort objektet på det angivna indexet från samlingen i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.webextensions/basewebextensioncollection/remove/
---
## BaseWebExtensionCollection::Remove method


Tar bort objektet på det angivna indexet från samlingen.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::Remove(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Det nollbaserade indexet för samlingselementet. |

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

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
