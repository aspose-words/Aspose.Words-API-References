---
title: "Aspose::Words::Markup::SdtDateStorageFormat enum"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. Anger hur datumet för ett datum‑SDT lagras/hämtas när SDT‑et är bundet till en XML‑nod i dokumentets datalager i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


Anger hur datumet för en datum‑SDT lagras/hämtas när SDT:n är bunden till en XML‑nod i dokumentets datalager.

```cpp
enum class SdtDateStorageFormat
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Datum | 0 | Datumvärdet för ett datum‑SDT lagras som ett datum i det standard‑XML‑Schema Date‑formatet. |
| DateTime | 1 | Datumvärdet för ett datum‑SDT lagras som ett datum i det standard‑XML‑Schema DateTime‑formatet. |
| Text | 2 | Datumvärdet för ett datum‑SDT lagras som text. |
| Default | n/a | Standardvärdet är [DateTime](./) |


## Exempel



Visar hur man uppmanar användaren att ange ett datum med en strukturerad dokumenttagg.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga en strukturerad dokumenttagg som uppmanar användaren att ange ett datum.
// I Microsoft Word kallas detta element för ett "Date picker content control".
// När vi klickar på pilen i högra änden av denna tagg i Microsoft Word,
// kommer vi att se en popup i form av en klickbar kalender.
// Vi kan använda den popupen för att välja ett datum som taggen kommer att visa.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Visa datumet enligt den saudisk-arabiska lokalen.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Ange formatet för hur datumet ska visas.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Visa datumet enligt den hijri‑kalendern.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Innan användaren väljer ett datum i Microsoft Word kommer taggen att visa texten "Click here to enter a date.".
// Enligt taggens kalender, ange egenskapen "FullDate" för att få taggen att visa ett standarddatum.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
