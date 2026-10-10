---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Version method"
linktitle: "get_Version"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Version method. Representa el número de versión de la aplicación que creó el documento en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_version/
---
## BuiltInDocumentProperties::get_Version method


Representa el número de versión de la aplicación que creó el documento.

```cpp
int32_t Aspose::Words::Properties::BuiltInDocumentProperties::get_Version()
```

## Observaciones


Cuando un documento fue creado por Microsoft Word, los 16 bits altos representan la versión principal y los 16 bits bajos representan el número de compilación.

## Ejemplos



Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".
```cpp
// Abra un documento que hemos creado y editado usando Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// Las siguientes propiedades integradas contienen información sobre la creación y edición de este documento.
// Podemos hacer clic derecho en este documento en el Explorador de Windows y encontrar
// estas propiedades a través de "Properties" -> "Details" -> categoría "Origin".
// Campos como PRINTDATE y EDITTIME pueden mostrar estos valores en el cuerpo del documento.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// También podemos cambiar los valores de las propiedades integradas.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word actualiza automáticamente las siguientes propiedades cuando guardamos el documento.
// Para usar estas propiedades con Aspose.Words, necesitaremos establecer sus valores manualmente.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// Podemos hacer clic derecho en este documento en el Explorador de Windows y encontrar estas propiedades en "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
