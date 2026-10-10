---
title: "Aspose::Words::Properties::CustomDocumentProperties clase"
linktitle: "CustomDocumentProperties"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::CustomDocumentProperties clase. Una colección de propiedades de documento personalizadas. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class


Una colección de propiedades de documento personalizadas. Para obtener más información, visite el artículo de documentación [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class CustomDocumentProperties : public Aspose::Words::Properties::DocumentPropertyCollection
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::String\&) | Crea una nueva propiedad de documento personalizada del tipo de datos [String](../propertytype/). |
| [Add](./add/)(const System::String\&, int32_t) | Crea una nueva propiedad de documento personalizada del tipo de datos [Number](../propertytype/). |
| [Add](./add/)(const System::String\&, System::DateTime) | Crea una nueva propiedad de documento personalizada del tipo de datos [DateTime](../propertytype/). |
| [Add](./add/)(const System::String\&, bool) | Crea una nueva propiedad de documento personalizada del tipo de datos [Boolean](../propertytype/). |
| [Add](./add/)(const System::String\&, double) | Crea una nueva propiedad de documento personalizada del tipo de datos [Double](../propertytype/). |
| [AddLinkToContent](./addlinktocontent/)(const System::String\&, const System::String\&) | Crea una nueva propiedad de documento personalizada vinculada al contenido. |
| [Clear](../documentpropertycollection/clear/)() | Elimina todas las propiedades de la colección. |
| [Contains](../documentpropertycollection/contains/)(const System::String\&) | Devuelve **true** si una propiedad con el nombre especificado existe en la colección. |
| [get_Count](../documentpropertycollection/get_count/)() | Obtiene el número de elementos en la colección. |
| [GetEnumerator](../documentpropertycollection/getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](../documentpropertycollection/idx_get/)(System::String) | Devuelve un objeto [DocumentProperty](../documentproperty/) por el nombre de la propiedad. |
| [idx_get](../documentpropertycollection/idx_get/)(int32_t) | Devuelve un objeto [DocumentProperty](../documentproperty/) por índice. |
| [IndexOf](../documentpropertycollection/indexof/)(const System::String\&) | Obtiene el índice de una propiedad por nombre. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../documentpropertycollection/remove/)(const System::String\&) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](../documentpropertycollection/removeat/)(int32_t) | Elimina una propiedad en el índice especificado. |
| static [Type](./type/)() |  |
## Observaciones


Cada objeto [DocumentProperty](../documentproperty/) representa una propiedad personalizada de un documento contenedor.

Los nombres de las propiedades no distinguen entre mayúsculas y minúsculas.

Las propiedades en la colección se ordenan alfabéticamente por nombre.

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

* Class [DocumentPropertyCollection](../documentpropertycollection/)
* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
