---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Markup.SdtDateStorageFormat förbättrar datumhanteringen i SDT:er och säkerställer sömlös XML-dataintegration i dina dokument.
type: docs
weight: 4700
url: /sv/net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Anger hur datumet för en datum-SDT lagras/hämtas när SDT:n är bunden till en XML-nod i dokumentets datalager.

```csharp
public enum SdtDateStorageFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Date | `0` | Datumvärdet för en datum-SDT lagras som ett datum i standardformatet för XML-schemadatum. |
| DateTime | `1` | Datumvärdet för en datum-SDT lagras som ett datum i standardformatet för XML-schemat DateTime. |
| Text | `2` | Datumvärdet för en datum-SDT lagras som text. |
| Default | `1` | StandardinställningDateTime |

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
