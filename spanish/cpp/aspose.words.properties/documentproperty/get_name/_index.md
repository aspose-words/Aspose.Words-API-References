---
title: "Aspose::Words::Properties::DocumentProperty::get_Name método"
linktitle: "get_Name"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::DocumentProperty::get_Name método. Devuelve el nombre de la propiedad en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.properties/documentproperty/get_name/
---
## DocumentProperty::get_Name method


Devuelve el nombre de la propiedad.

```cpp
System::String Aspose::Words::Properties::DocumentProperty::get_Name() const
```

## Observaciones


No puede ser **null** y no puede ser una cadena vacía.

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
