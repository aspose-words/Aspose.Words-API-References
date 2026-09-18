---
title: "Aspose::Words::Fields::FieldDate::get_UseLastFormat method"
linktitle: "get_UseLastFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldDate::get_UseLastFormat method. Liest oder setzt, ob ein Format verwendet wird, das zuletzt von der hostenden Anwendung verwendet wurde, wenn ein neues DATE-Feld in C++ eingefügt wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fielddate/get_uselastformat/
---
## FieldDate::get_UseLastFormat method


Ruft ab oder legt fest, ob beim Einfügen eines neuen DATE‑Felds ein vom Host‑Programm zuletzt verwendetes Format verwendet werden soll.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLastFormat()
```


## Beispiele



Zeigt, wie DATE‑Felder verwendet werden, um Daten gemäß verschiedener Kalenderarten anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir möchten, dass der Text im Dokument stets das korrekte Datum anzeigt, können wir ein DATE‑Feld verwenden.
// Im Folgenden sind drei Arten von Kulturkalendern aufgeführt, die ein DATE‑Feld zur Anzeige eines Datums verwenden kann.
// 1 -  Islamischer Mondkalender:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al‑Qura‑Kalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Indischer Nationalkalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Fügen Sie ein DATE‑Feld ein und setzen Sie dessen Kalendertyp auf den zuletzt vom Host‑Programm verwendeten.
// In Microsoft Word wird der Typ der zuletzt im Dialogfeld Einfügen → Text → Datum und Uhrzeit verwendet.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Siehe auch

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
