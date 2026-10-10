---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get método"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::idx_get método. Devuelve un objeto DocumentProperty por el nombre de la propiedad en C++."
type: docs
weight: 35000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/idx_get/
---
## BuiltInDocumentProperties::idx_get method


Devuelve un objeto [DocumentProperty](../../documentproperty/) por el nombre de la propiedad.

```cpp
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> Aspose::Words::Properties::BuiltInDocumentProperties::idx_get(System::String name) override
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | System::String | El nombre de la propiedad a recuperar, sin distinción de mayúsculas y minúsculas. |
## Observaciones


Los nombres de cadena de las propiedades corresponden a los nombres de las propiedades tipadas disponibles en [BuiltInDocumentProperties](../).

Si solicita una propiedad que no está presente en el documento, pero el nombre de la propiedad se reconoce como un nombre incorporado válido, se crea una nueva [DocumentProperty](../../documentproperty/), se agrega a la colección y se devuelve. La propiedad recién creada se asigna con un valor predeterminado (cadena vacía, cero, **false** o DateTime.MinValue según el tipo de la propiedad incorporada).

Si solicita una propiedad que no está presente en el documento y el nombre no se reconoce como un nombre incorporado, se devuelve un **null**.

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
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
