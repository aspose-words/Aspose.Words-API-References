---
title: "Metodo get_UseUmAlQuraCalendar di Aspose::Words::Fields::FieldCreateDate"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_UseUmAlQuraCalendar di Aspose::Words::Fields::FieldCreateDate. Ottiene o imposta se utilizzare il calendario Um-al-Qura in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/fieldcreatedate/get_useumalquracalendar/
---
## FieldCreateDate::get_UseUmAlQuraCalendar method


Ottiene o imposta se utilizzare il calendario Um-al-Qura.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseUmAlQuraCalendar() override
```


## Esempi



Mostra come utilizzare il campo CREATEDATE per visualizzare la data/ora di creazione del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// Possiamo utilizzare il campo CREATEDATE per visualizzare la data e l'ora di creazione del documento.
// Di seguito sono riportati tre diversi tipi di calendario in base ai quali il campo CREATEDATE può visualizzare la data/ora.
// 1 -  Calendario lunare islamico:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Calendario Umm al-Qura:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  Calendario nazionale indiano:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## Vedi anche

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
