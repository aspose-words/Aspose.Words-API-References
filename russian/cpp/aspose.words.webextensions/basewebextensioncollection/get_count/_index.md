---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::get_Count метод"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::get_Count метод. Получает количество элементов, содержащихся в коллекции, в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.webextensions/basewebextensioncollection/get_count/
---
## BaseWebExtensionCollection::get_Count method


Получает количество элементов, содержащихся в коллекции.

```cpp
int32_t Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::get_Count()
```


## Примеры



Показывает, как работать с коллекцией веб‑расширений документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Выводит все свойства веб‑расширения документа.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Удалить веб-расширение.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## См. также

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
