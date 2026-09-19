---
title: "Metodo Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar"
linktitle: "get_UseSakaEraCalendar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar. Ottiene o imposta se utilizzare il calendario Saka Era in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldsavedate/get_usesakaeracalendar/
---
## FieldSaveDate::get_UseSakaEraCalendar method


Ottiene o imposta se utilizzare il calendario dell'Era Saka.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseSakaEraCalendar() override
```


## Esempi



Mostra come utilizzare il campo SAVEDATE per visualizzare data/ora dell'operazione di salvataggio più recente del documento eseguita con Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// Possiamo usare il campo SAVEDATE per visualizzare data e ora dell'ultima operazione di salvataggio sul documento.
// L'operazione di salvataggio a cui si riferiscono questi campi è il salvataggio manuale in un'applicazione come Microsoft Word,
// non il metodo Save del documento.
// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo SAVEDATE può visualizzare data/ora.
// 1 -  Calendario lunare islamico:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Calendario Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - Calendario nazionale indiano:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// I campi SAVEDATE prendono i loro valori di data/ora dalla proprietà incorporata LastSavedTime.
// Il metodo Save del documento non aggiornerà questo valore, ma possiamo comunque aggiornarlo manualmente.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## Vedi anche

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
