---
title: "Método Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar"
linktitle: "get_UseLunarCalendar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar. Obtiene o establece si se usa el calendario lunar Hijri o el calendario lunar Hebreo en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldsavedate/get_uselunarcalendar/
---
## FieldSaveDate::get_UseLunarCalendar method


Obtiene o establece si se debe usar el calendario lunar hijri o el calendario lunar hebreo.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar() override
```


## Ejemplos



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

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
