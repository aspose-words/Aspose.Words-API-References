---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_FullDate metodo"
linktitle: "get_FullDate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_FullDate metodo. Specifica la data e l'ora complete inserite più recentemente in questo SDT in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_fulldate/
---
## StructuredDocumentTag::get_FullDate method


Specifica la data e l'ora complete inserite più recentemente in questo **SDT**.

```cpp
System::DateTime Aspose::Words::Markup::StructuredDocumentTag::get_FullDate()
```

## Note


L'accesso a questa proprietà funzionerà solo per il tipo SDT [Date](../../sdttype/).

Per tutti gli altri tipi SDT si verificherà un'eccezione.

## Esempi



Mostra come chiedere all'utente di inserire una data con un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci un tag di documento strutturato che richiede all'utente di inserire una data.
// In Microsoft Word, questo elemento è conosciuto come "Date picker content control".
// Quando facciamo clic sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo un pop up nella forma di un calendario cliccabile.
// Possiamo usare quel pop‑up per selezionare una data che il tag visualizzerà.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Visualizza la data, secondo le impostazioni locali arabo‑saudite.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Imposta il formato con cui visualizzare la data.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Visualizza la data secondo il calendario Hijri.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Click here to enter a date.".
// Secondo il calendario del tag, imposta la proprietà "FullDate" per far visualizzare al tag una data predefinita.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
