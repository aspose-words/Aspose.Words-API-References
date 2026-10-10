---
title: "Método Aspose::Words::Properties::DocumentPropertyCollection::idx_get"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::DocumentPropertyCollection::idx_get. Devuelve un objeto DocumentProperty por índice en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.properties/documentpropertycollection/idx_get/
---
## DocumentPropertyCollection::idx_get(int32_t) method


Devuelve un objeto [DocumentProperty](../../documentproperty/) por índice.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | Índice basado en cero del [DocumentProperty](../../documentproperty/) a recuperar. |

## Ejemplos



Muestra cómo trabajar con propiedades de documento personalizadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Cada documento contiene una colección de propiedades personalizadas, que, al igual que las propiedades incorporadas, son pares clave-valor.
// El documento tiene una lista fija de propiedades incorporadas. El usuario crea todas las propiedades personalizadas.
ASSERT_EQ(u"Value of custom document property", System::ObjectExt::ToString(doc->get_CustomDocumentProperties()->idx_get(u"CustomProperty")));

doc->get_CustomDocumentProperties()->Add(u"CustomProperty2", System::String(u"Value of custom document property #2"));

std::cout << "Custom Properties:" << std::endl;
for (auto&& customDocumentProperty : System::IterateOver(doc->get_CustomDocumentProperties()))
{
    std::cout << customDocumentProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", customDocumentProperty->get_Type()) << std::endl;
    std::cout << System::String::Format(u"\tValue:\t\"{0}\"", customDocumentProperty->get_Value()) << std::endl;
}
```

## Ver también

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentPropertyCollection::idx_get(System::String) method


Devuelve un objeto [DocumentProperty](../../documentproperty/) por el nombre de la propiedad.

```cpp
virtual System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::DocumentPropertyCollection::idx_get(System::String name)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | System::String | El nombre de la propiedad a recuperar, sin distinción de mayúsculas y minúsculas. |
## Observaciones


Devuelve **null** si no se encuentra una propiedad con el nombre especificado.

## Ejemplos



Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y hora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

doc->get_CustomDocumentProperties()->Add(u"AuthorizationDate", System::DateTime::get_Now());
System::DateTime authorizationDate = doc->get_CustomDocumentProperties()->idx_get(u"AuthorizationDate")->ToDateTime();
std::cout << System::String::Format(u"Document authorized on {0}", authorizationDate) << std::endl;
```

## Ver también

* Class [DocumentProperty](../../documentproperty/)
* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
