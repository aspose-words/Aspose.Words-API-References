---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Title método"
linktitle: "get_Title"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Title método. Obtiene o establece el título del documento en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_title/
---
## BuiltInDocumentProperties::get_Title method


Obtiene o establece el título del documento.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_Title()
```


## Ejemplos



Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// A continuación se presentan cuatro propiedades de documento incorporadas que tienen campos que pueden mostrar sus valores en el cuerpo del documento.
// 1 -  "Author" propiedad, que podemos mostrar usando un campo AUTHOR:
properties->set_Author(u"John Doe");
builder->Write(u"Author:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true);

// 2 -  "Title" propiedad, que podemos mostrar usando un campo TITLE:
properties->set_Title(u"John's Document");
builder->Write(u"\nDoc title:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, true);

// 3 -  "Subject" propiedad, que podemos mostrar usando un campo SUBJECT:
properties->set_Subject(u"My subject");
builder->Write(u"\nSubject:\t");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true);

// 4 -  "Comments" propiedad, que podemos mostrar usando un campo COMMENTS:
properties->set_Comments(System::String::Format(u"This is {0}'s document about {1}", properties->get_Author(), properties->get_Subject()));
builder->Write(u"\nComments:\t\"");
builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true);
builder->Write(u"\"");

// La "Category" propiedad incorporada no tiene un campo que pueda mostrar su valor.
properties->set_Category(u"My category");

// Podemos establecer varias palabras clave para un documento separando el valor de cadena de la propiedad "Keywords" con punto y coma.
properties->set_Keywords(u"Tag 1; Tag 2; Tag 3");

// Podemos hacer clic derecho en este documento en el Explorador de Windows y encontrar estas propiedades en "Properties" -> "Details".
// La "Author" propiedad incorporada está en el grupo "Origin", y las demás están en el grupo "Description".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Description.docx");
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
