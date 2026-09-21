---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale metod"
linktitle: "get_DateDisplayLocale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale metod. Tillåter att ange/hämta språkformatet för datumet som visas i denna SDT i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_datedisplaylocale/
---
## StructuredDocumentTag::get_DateDisplayLocale method


Tillåter att ange/hämta språkformatet för datumet som visas i detta **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_DateDisplayLocale()
```

## Anmärkningar


Att komma åt den här egenskapen fungerar endast för [Date](../../sdttype/) SDT-typ.

För alla andra SDT-typer kommer ett undantag att uppstå.

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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
