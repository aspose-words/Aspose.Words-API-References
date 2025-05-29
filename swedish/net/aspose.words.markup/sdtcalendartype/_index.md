---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words för .NET
description: Utforska Aspose.Words.Markup.SdtCalendarType-enum för att förbättra dina Office Open XML-dokument med mångsidiga kalenderalternativ för bättre arbetsflödeseffektivitet.
type: docs
weight: 4690
url: /sv/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Anger de möjliga typerna av kalendrar som kan användas för att ange[`CalendarType`](../structureddocumenttag/calendartype/) i ett Office Open XML-dokument.

```csharp
public enum SdtCalendarType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Används som standardvärde i OOXML. Lika medGregorian . |
| Gregorian | `0` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Denna kalender ska lokaliseras till lämpligt språk. |
| GregorianArabic | `1` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Värdena för denna kalender ska presenteras på arabiska. |
| GregorianMeFrench | `2` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Värdena för denna kalender ska presenteras på mellanösternfranska. |
| GregorianUs | `3` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Värdena för denna kalender ska presenteras på engelska. |
| GregorianXlitEnglish | `4` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Värdena för denna kalender ska representera de engelska strängarna med motsvarande arabiska tecken (den arabiska translitterationen av den engelska för den gregorianska kalendern). |
| GregorianXlitFrench | `5` | Anger att den gregorianska kalendern, enligt definitionen i ISO 8601, ska användas. Värdena för denna kalender ska representera de franska strängarna med motsvarande arabiska tecken (den arabiska translitterationen av den franska för den gregorianska kalendern). |
| Hebrew | `6` | Anger att den hebreiska månkalendern, såsom den beskrivs av Gauss formel för påsk [CITATION] och Den fullständiga omformuleringen av muntlig lag (Mishneh Torah), ska användas. |
| Hijri | `7` | Anger att Hijri-månkalendern, såsom den beskrivs av Saudiarabien, Ministeriet för islamiska frågor, stiftelser, Da'wah och vägledning, ska användas. |
| Japan | `8` | Anger att den japanska kejsartidens kalender, enligt beskrivningen i japansk industristandard JIS X 0301, ska användas. |
| Korea | `9` | Anger att den koreanska Tangun-erans kalender, enligt beskrivningen i koreansk lagförordning nr 4, ska användas. |
| None | `10` | Anger att ingen kalender ska användas. |
| Saka | `11` | Anger att Saka-erakalendern, så som den beskrivs av Indiens kalenderreformkommitté, som en del av den indiska efemeriden och den nautiska almanackan, ska användas. |
| Taiwan | `12` | Anger att den taiwanesiska kalendern, enligt definitionen i den kinesiska nationella standarden CNS 7648, ska användas. |
| Thai | `13` | Anger att den thailändska kalendern, såsom den definieras i det kungliga dekretet från HM kung Vajiravudh (Rama VI) i Royal Gazette BE 2456 (1913 e.Kr.) och i premiärminister Phibunsongkhrams dekret (1941 e.Kr.) för att börja året den gregorianska 1 januari och koppla år noll till det gregorianska året 543 f.Kr., ska användas. |

## Exempel

Visar hur man uppmanar användaren att ange ett datum med en strukturerad dokumenttagg.

```csharp
Document doc = new Document();

// Infoga en strukturerad dokumenttagg som uppmanar användaren att ange ett datum.
// I Microsoft Word kallas detta element för en "Datumväljarens innehållskontroll".
// När vi klickar på pilen till höger om den här taggen i Microsoft Word,
// vi kommer att se ett popup-fönster i form av en klickbar kalender.
// Vi kan använda den popup-filen för att välja ett datum som taggen ska visa.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Visa datumet enligt den saudiarabiska språkinställningen.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Ange formatet som datumet ska visas med.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Visar datumet enligt Hijri-kalendern.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Innan användaren väljer ett datum i Microsoft Word visar taggen texten "Klicka här för att ange ett datum.".
// Enligt taggens kalender, ställ in egenskapen "FullDate" för att få taggen att visa ett standarddatum.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
