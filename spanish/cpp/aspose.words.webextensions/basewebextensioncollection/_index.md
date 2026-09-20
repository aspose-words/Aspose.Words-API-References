---
title: "Clase Aspose::Words::WebExtensions::BaseWebExtensionCollection"
linktitle: "BaseWebExtensionCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::WebExtensions::BaseWebExtensionCollection. Clase base para las colecciones TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection y WebExtensionReferenceCollection. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Clase base para las colecciones [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) y [WebExtensionReferenceCollection](../webextensionreferencecollection/). Para obtener más información, visite el artículo de documentación [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parámetro | Descripción |
| --- | --- |
| T | Tipo de un elemento de la colección. |
## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(T) | Agrega el elemento especificado a la colección. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Elimina todos los elementos de la colección. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Obtiene el número de elementos contenidos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un enumerador que puede iterar a través de una colección. |
| [idx_get](./idx_get/)(int32_t) | Obtiene o establece un elemento en el índice especificado. |
| [idx_set](./idx_set/)(int32_t, T) | Obtiene o establece un elemento en el índice especificado. |
| [Remove](./remove/)(int32_t) | Elimina el elemento en el índice especificado de la colección. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descripción |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
