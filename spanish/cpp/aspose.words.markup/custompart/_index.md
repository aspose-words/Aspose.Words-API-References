---
title: "Clase Aspose::Words::Markup::CustomPart"
linktitle: "CustomPart"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Markup::CustomPart. Representa una parte personalizada (contenido arbitrario) que no está definida por la norma ISO/IEC 29500. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Representa una parte personalizada (contenido arbitrario) que no está definida por la norma ISO/IEC 29500. Para obtener más información, visite el artículo de documentación [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Crea una copia "suficientemente profunda" del objeto. No duplica los bytes del valor [Data](./get_data/). |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Especifica el tipo de contenido de esta parte personalizada. |
| [get_Data](./get_data/)() const | Contiene los datos de esta parte personalizada. |
| [get_IsExternal](./get_isexternal/)() const | Falso si esta parte personalizada se almacena dentro del paquete OOXML. Verdadero si esta parte personalizada es un objetivo externo. |
| [get_Name](./get_name/)() const | Obtiene o establece el nombre absoluto de esta parte dentro del paquete OOXML o la URL de destino. |
| [get_RelationshipType](./get_relationshiptype/)() const | Obtiene o establece el tipo de relación del elemento principal a esta parte personalizada. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Establecedor de [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Establecedor de [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Establecedor de [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Establecedor de [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Establecedor de [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Observaciones


Esta clase representa una parte OOXML que es objetivo de una "relación desconocida". Todas las relaciones no definidas dentro de la ISO/IEC 29500 se consideran "relaciones desconocidas". Las relaciones desconocidas están permitidas dentro de un documento Office Open XML siempre que cumplan con las directrices de marcado de relaciones.

Microsoft Word conserva las partes personalizadas durante los ciclos de apertura/guardado. Se puede encontrar información adicional aquí [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words también mantiene las partes personalizadas en los procesos de lectura/escritura y, además, permite acceder programáticamente a dichas partes mediante los objetos [CustomPart](./) y [CustomPartCollection](../custompartcollection/).

No confunda las partes personalizadas con datos XML personalizados. Use [CustomXmlPart](../customxmlpart/) si necesita acceder a datos XML personalizados.

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
