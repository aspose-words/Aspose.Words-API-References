---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::GetEnumerator método. Devuelve un enumerador que puede iterar a través de una colección en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.webextensions/basewebextensioncollection/getenumerator/
---
## BaseWebExtensionCollection::GetEnumerator method


Devuelve un enumerador que puede iterar a través de una colección.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<T>> Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::GetEnumerator() override
```


## Ejemplos



Muestra cómo trabajar con la colección de extensiones web de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Imprime todas las propiedades de la extensión web del documento.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Eliminar la extensión web.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## Ver también

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
