---
title: "Aspose::Words::Properties::DocumentPropertyCollection::get_Count método"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::DocumentPropertyCollection::get_Count. Obtiene el número de elementos en la colección en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.properties/documentpropertycollection/get_count/
---
## DocumentPropertyCollection::get_Count method


Obtiene el número de elementos en la colección.

```cpp
int32_t Aspose::Words::Properties::DocumentPropertyCollection::get_Count()
```


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

* Class [DocumentPropertyCollection](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
