---
title: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar metodo"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar metodo. Ottiene o imposta se utilizzare il calendario Um-al-Qura in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fields/fielddate/get_useumalquracalendar/
---
## FieldDate::get_UseUmAlQuraCalendar method


Ottiene o imposta se utilizzare il calendario Um-al-Qura.

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar() override
```


## Esempi



Mostra come utilizzare i campi DATE per visualizzare le date secondo diversi tipi di calendari.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se vogliamo che il testo nel documento mostri sempre la data corretta, possiamo usare un campo DATE.
// Di seguito sono riportati tre tipi di calendari culturali che un campo DATE può utilizzare per visualizzare una data.
// 1 -  Calendario lunare islamico:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Calendario Umm al-Qura:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Calendario nazionale indiano:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Inserisci un campo DATE e imposta il suo tipo di calendario a quello usato per ultimo dall'applicazione host.
// In Microsoft Word, il tipo sarà quello più recentemente usato nella finestra di dialogo Inserisci -> Testo -> Data e ora.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Vedi anche

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
