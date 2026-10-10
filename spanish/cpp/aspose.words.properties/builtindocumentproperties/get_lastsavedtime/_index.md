---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime método"
linktitle: "get_LastSavedTime"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime método. Obtiene o establece la hora del último guardado en UTC en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


Obtiene o establece la hora del último guardado en UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## Observaciones


Para documentos originados en formato RTF, esta propiedad devuelve la hora local de la última operación de guardado.

Aspose.Words no actualiza esta propiedad.

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


Muestra cómo usar el campo SAVEDATE para mostrar la fecha/hora de la operación de guardado más reciente del documento realizada con Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Podemos usar el campo SAVEDATE para mostrar la fecha y hora de la última operación de guardado en el documento.
// La operación de guardado a la que se refieren estos campos es el guardado manual en una aplicación como Microsoft Word,
// no el método Save del documento.
// A continuación se presentan tres tipos de calendario diferentes según los cuales el campo SAVEDATE puede mostrar la fecha/hora.
// 1 -  Calendario lunar islámico:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Calendario Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - Calendario nacional indio:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Los campos SAVEDATE obtienen sus valores de fecha/hora de la propiedad incorporada LastSavedTime.
// El método Save del documento no actualizará este valor, pero aún podemos actualizarlo manualmente.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
