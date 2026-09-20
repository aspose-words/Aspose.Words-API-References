---
title: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar método"
linktitle: "get_UseLunarCalendar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar método. Obtiene o establece si se debe usar el calendario lunar Hijri o el calendario lunar Hebreo en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fielddate/get_uselunarcalendar/
---
## FieldDate::get_UseLunarCalendar method


Obtiene o establece si se debe usar el calendario lunar hijri o el calendario lunar hebreo.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLunarCalendar() override
```


## Ejemplos



Muestra cómo usar campos DATE para mostrar fechas según diferentes tipos de calendarios.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si queremos que el texto del documento siempre muestre la fecha correcta, podemos usar un campo DATE.
// A continuación se presentan tres tipos de calendarios culturales que un campo DATE puede usar para mostrar una fecha.
// 1 -  Calendario lunar islámico:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Calendario Umm al-Qura:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Calendario nacional indio:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Inserte un campo DATE y establezca su tipo de calendario al que fue usado por última vez por la aplicación anfitriona.
// En Microsoft Word, el tipo será el más usado recientemente en el cuadro de diálogo Insertar -> Texto -> Fecha y hora.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Ver también

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
