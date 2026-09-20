---
title: "Aspose::Words::Properties::DocumentPropertyCollection clase"
linktitle: "DocumentPropertyCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::DocumentPropertyCollection class. Clase base para las colecciones BuiltInDocumentProperties y CustomDocumentProperties. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Clase base para las colecciones [BuiltInDocumentProperties](../builtindocumentproperties/) y [CustomDocumentProperties](../customdocumentproperties/). Para obtener más información, visite el artículo de documentación [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Elimina todas las propiedades de la colección. |
| [Contains](./contains/)(const System::String\&) | Devuelve **true** si una propiedad con el nombre especificado existe en la colección. |
| [get_Count](./get_count/)() | Obtiene el número de elementos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador que puede usarse para iterar sobre todos los elementos de la colección. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Devuelve un objeto [DocumentProperty](../documentproperty/) por el nombre de la propiedad. |
| [idx_get](./idx_get/)(int32_t) | Devuelve un objeto [DocumentProperty](../documentproperty/) por índice. |
| [IndexOf](./indexof/)(const System::String\&) | Obtiene el índice de una propiedad por nombre. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](./removeat/)(int32_t) | Elimina una propiedad en el índice especificado. |
| static [Type](./type/)() |  |
## Observaciones


Los nombres de las propiedades no distinguen entre mayúsculas y minúsculas.

Las propiedades en la colección se ordenan alfabéticamente por nombre.

## Ejemplos



Muestra cómo trabajar con las propiedades personalizadas de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Las propiedades personalizadas del documento son pares clave-valor que podemos añadir al documento.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La colección ordena las propiedades personalizadas alfabéticamente.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Imprima cada propiedad personalizada del documento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Muestre el valor de una propiedad personalizada usando un campo DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Podemos encontrar estas propiedades personalizadas en Microsoft Word a través de "File" -> "Properties" > "Advanced Properties" > "Custom".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// A continuación se presentan tres formas de eliminar propiedades personalizadas de un documento.
// 1 -  Eliminar por índice:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Eliminar por nombre:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Vaciar toda la colección de una vez:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Ver también

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
