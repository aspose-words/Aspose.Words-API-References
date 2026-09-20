---
title: "Clase Aspose::Words::Properties::DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Properties::DocumentProperty. Representa una propiedad de documento personalizada o incorporada. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Representa una propiedad de documento personalizada o incorporada. Para obtener más información, visite el artículo de documentación [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Muestra si esta propiedad está vinculada al contenido o no. |
| [get_LinkSource](./get_linksource/)() const | Obtiene la fuente de una propiedad de documento personalizada vinculada. |
| [get_Name](./get_name/)() const | Devuelve el nombre de la propiedad. |
| [get_Type](./get_type/)() const | Obtiene el tipo de datos de la propiedad. |
| [get_Value](./get_value/)() | Obtiene o establece el valor de la propiedad. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Método setter para [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Devuelve el valor de la propiedad como bool. |
| [ToByteArray](./tobytearray/)() | Devuelve el valor de la propiedad como matriz de bytes. |
| [ToDateTime](./todatetime/)() | Devuelve el valor de la propiedad como **DateTime** en UTC. |
| [ToDouble](./todouble/)() | Devuelve el valor de la propiedad como double. |
| [ToInt](./toint/)() | Devuelve el valor de la propiedad como integer. |
| [ToString](./tostring/)() const override | Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo trabajar con las propiedades de documento incorporadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// El objeto "Document" contiene parte de sus metadatos en sus miembros.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// El documento también almacena metadatos en sus propiedades incorporadas.
// Cada propiedad incorporada es un miembro del objeto "BuiltInDocumentProperties" del documento.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Algunas propiedades pueden almacenar múltiples valores.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Ver también

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
