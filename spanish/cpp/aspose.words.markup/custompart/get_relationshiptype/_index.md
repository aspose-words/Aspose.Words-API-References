---
title: "Aspose::Words::Markup::CustomPart::get_RelationshipType método"
linktitle: "get_RelationshipType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::CustomPart::get_RelationshipType método. Obtiene o establece el tipo de relación desde la parte principal a esta parte personalizada en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.markup/custompart/get_relationshiptype/
---
## CustomPart::get_RelationshipType method


Obtiene o establece el tipo de relación del elemento principal a esta parte personalizada.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_RelationshipType() const
```

## Observaciones


El tipo de relación para una parte personalizada debe ser "unknown", p. ej. un tipo de relación personalizado, no uno de los tipos de relación definidos dentro de ISO/IEC 29500.

El valor predeterminado es una cadena vacía. Un valor válido debe ser una cadena no vacía.

## Ejemplos



Muestra cómo acceder a la colección de partes personalizadas arbitrarias de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clona la segunda parte, luego agrega el clon a la colección.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumere la colección e imprima cada parte.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Podemos eliminar elementos de esta colección individualmente, o todos a la vez.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Ver también

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
