---
title: "Aspose::Words::Markup::SdtCalendarType enum"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::SdtCalendarType enum. Anger de möjliga kalendertyper som kan användas för att specificera CalendarType i ett Office Open XML‑dokument i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Anger de möjliga kalendertyper som kan användas för att specificera [CalendarType](../structureddocumenttag/get_calendartype/) i ett Office Open XML‑dokument.

```cpp
enum class SdtCalendarType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | 0 | Används som standardvärde i OOXML. Motsvarar [Gregorian](./). |
| Gregoriansk | n/a | Anger att den gregorianska kalendern, enligt ISO 8601, ska användas. Denna kalender bör lokalanpassas till lämpligt språk. |
| GregorianArabic | n/a | Anger att den gregorianska kalendern, enligt ISO 8601, ska användas. Värdena för denna kalender bör presenteras på arabiska. |
| GregorianMeFrench | n/a | Anger att den gregorianska kalendern, enligt definition i ISO 8601, ska användas. Värdena för denna kalender bör presenteras på Mellanösternfranska. |
| GregorianUs | n/a | Anger att den gregorianska kalendern, enligt definition i ISO 8601, ska användas. Värdena för denna kalender bör presenteras på engelska. |
| GregorianXlitEnglish | n/a | Anger att den gregorianska kalendern, enligt definition i ISO 8601, ska användas. Värdena för denna kalender bör vara representationen av de engelska strängarna i motsvarande arabiska tecken (den arabiska translitterationen av engelskan för den gregorianska kalendern). |
| GregorianXlitFrench | n/a | Anger att den gregorianska kalendern, enligt definition i ISO 8601, ska användas. Värdena för denna kalender bör vara representationen av de franska strängarna i motsvarande arabiska tecken (den arabiska translitterationen av franskan för den gregorianska kalendern). |
| Hebreiska | n/a | Anger att den hebreiska månkalendern, enligt Gauss formel för påsk [CITATION] och The Complete Restatement of Oral Law (Mishneh Torah), ska användas. |
| Hijri | n/a | Anger att den hijri månkalendern, enligt Kungariket Saudiarabien, Ministeriet för islamiska frågor, donationer, Da‘wah och vägledning, ska användas. |
| Japan | n/a | Anger att den japanska kejsarepoken kalendern, enligt Japansk industriell standard JIS X 0301, ska användas. |
| Korea | n/a | Anger att den koreanska Tangun-eran kalendern, enligt Koreansk lagstiftning nr 4, ska användas. |
| None | n/a | Anger att ingen kalender ska användas. |
| Saka | n/a | Anger att Saka-eran kalendern, enligt Calendar Reform Committee of India, som en del av den indiska ephemeriden och nautiska almanackan, ska användas. |
| Taiwan | n/a | Anger att den taiwanesiska kalendern, enligt den kinesiska nationella standarden CNS 7648, ska användas. |
| Thai | n/a | Anger att den thailändska kalendern, enligt Kungliga dekretet av H.M. Kung Vajiravudh (Rama VI) i Royal Gazette B. E. 2456 (1913 e.Kr.) och genom dekretet av premiärminister Phibunsongkhram (1941 e.Kr.) för att starta året den gregorianska 1 januari och mappa år noll till den gregorianska år 543 f.Kr., ska användas. |


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
