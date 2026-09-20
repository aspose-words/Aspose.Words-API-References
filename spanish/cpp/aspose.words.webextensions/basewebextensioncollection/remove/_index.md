---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove método"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove método. Elimina el elemento en el índice especificado de la colección en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.webextensions/basewebextensioncollection/remove/
---
## BaseWebExtensionCollection::Remove method


Elimina el elemento en el índice especificado de la colección.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::Remove(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero del elemento de la colección. |

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
