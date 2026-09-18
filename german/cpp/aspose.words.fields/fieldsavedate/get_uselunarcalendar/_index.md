---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar method"
linktitle: "get_UseLunarCalendar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar method. Liest oder setzt, ob der Hijri-Lunar- oder Hebräisch-Lunar-Kalender in C++ verwendet wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldsavedate/get_uselunarcalendar/
---
## FieldSaveDate::get_UseLunarCalendar method


Liest oder setzt, ob der islamische Mondkalender oder der hebräische Mondkalender verwendet wird.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar() override
```


## Beispiele



Zeigt, wie das SAVEDATE‑Feld verwendet wird, um das Datum/Uhrzeit der zuletzt in Microsoft Word durchgeführten Speicheroperation des Dokuments anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Wir können das SAVEDATE‑Feld verwenden, um das Datum und die Uhrzeit der letzten Speicheroperation im Dokument anzuzeigen.
// Die Speicheroperation, auf die sich diese Felder beziehen, ist das manuelle Speichern in einer Anwendung wie Microsoft Word,
// nicht die Save‑Methode des Dokuments.
// Im Folgenden sind drei verschiedene Kalendertypen aufgeführt, nach denen das SAVEDATE‑Feld Datum/Uhrzeit anzeigen kann.
// 1 -  Islamischer Mondkalender:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al‑Qura‑Kalender:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 -  Indischer Nationalkalender:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// Die SAVEDATE‑Felder beziehen ihre Datums-/Uhrzeitwerte aus der integrierten Eigenschaft LastSavedTime.
// Die Save‑Methode des Dokuments aktualisiert diesen Wert nicht, aber wir können ihn dennoch manuell aktualisieren.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Siehe auch

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
