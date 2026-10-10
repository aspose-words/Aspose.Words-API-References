---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar Methode"
linktitle: "get_UseSakaEraCalendar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar method. Gibt an, ob der Saka-Ära-Kalender in C++ verwendet wird, oder legt ihn fest."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldcreatedate/get_usesakaeracalendar/
---
## FieldCreateDate::get_UseSakaEraCalendar method


Liest oder setzt, ob der Saka‑Eras‑Kalender verwendet wird.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar() override
```


## Beispiele



Zeigt, wie das CREATEDATE‑Feld verwendet wird, um das Erstellungsdatum/-zeit des Dokuments anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Wir können das CREATEDATE‑Feld verwenden, um das Datum und die Uhrzeit der Dokumentenerstellung anzuzeigen.
// Im Folgenden sind drei verschiedene Kalendertypen aufgeführt, nach denen das CREATEDATE‑Feld Datum/Zeit anzeigen kann.
// 1 -  Islamischer Mondkalender:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al‑Qura‑Kalender:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Indischer Nationalkalender:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Siehe auch

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
