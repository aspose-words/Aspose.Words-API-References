---
title: "Aspose::Words::Properties::PropertyType enum"
linktitle: "PropertyType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::PropertyType enum. Especifica el tipo de datos de una propiedad del documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.properties/propertytype/
---
## PropertyType enum


Especifica el tipo de datos de una propiedad de documento.

```cpp
enum class PropertyType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Boolean | 0 | La propiedad es un valor booleano. |
| DateTime | 1 | La propiedad es un valor de fecha y hora. |
| Double | 2 | La propiedad es un número de punto flotante. |
| Number | 3 | La propiedad es un número entero. |
| String | 4 | La propiedad es un valor de cadena. |
| StringArray | 5 | La propiedad es una matriz de cadenas. |
| ObjectArray | 6 | La propiedad es una matriz de objetos. |
| ByteArray | 7 | La propiedad es una matriz de bytes. |
| Otro | 8 | La propiedad es de otro tipo. |


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
