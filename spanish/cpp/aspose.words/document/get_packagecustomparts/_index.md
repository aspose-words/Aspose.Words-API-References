---
title: "Aspose::Words::Document::get_PackageCustomParts método"
linktitle: "get_PackageCustomParts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_PackageCustomParts método. Obtiene o establece la colección de partes personalizadas (contenido arbitrario) que están vinculadas al paquete OOXML usando \"unknown relationships\" en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


Obtiene o establece la colección de partes personalizadas (contenido arbitrario) que están vinculadas al paquete OOXML usando "relaciones desconocidas".

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## Observaciones


No confunda estas partes personalizadas con Custom XML Data. Si necesita acceder a partes Custom XML, use la propiedad [CustomXmlParts](../get_customxmlparts/).

Esta colección contiene partes OOXML cuyo padre es el paquete OOXML y sus destinos son de una "unknown relationship". Para más información vea [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words solo carga y guarda partes personalizadas en documentos OOXML.

Esta propiedad no puede ser **null**.

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

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
