---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar método"
linktitle: "get_UseLunarCalendar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar método. Obtiene o establece si se debe usar el calendario lunar Hijri o el calendario lunar Hebreo en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldcreatedate/get_uselunarcalendar/
---
## FieldCreateDate::get_UseLunarCalendar method


Obtiene o establece si se debe usar el calendario lunar hijri o el calendario lunar hebreo.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar() override
```


## Ejemplos



Muestra cómo usar el campo CREATEDATE para mostrar la fecha/hora de creación del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Podemos usar el campo CREATEDATE para mostrar la fecha y hora de la creación del documento.
// A continuación se presentan tres tipos de calendario diferentes según los cuales el campo CREATEDATE puede mostrar la fecha/hora.
// 1 -  Calendario lunar islámico:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Calendario Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Calendario nacional indio:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Ver también

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
