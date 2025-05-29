---
title: StructuredDocumentTag.DateStorageFormat
linktitle: DateStorageFormat
articleTitle: DateStorageFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen StructuredDocumentTag DateStorageFormat för att enkelt hantera datumformat i XML-bundna SDT:er och förbättra dokumentets dataorganisation.
type: docs
weight: 110
url: /sv/net/aspose.words.markup/structureddocumenttag/datestorageformat/
---
## StructuredDocumentTag.DateStorageFormat property

Hämtar/ställer in formatet i vilket datumet för en datum-SDT lagras när**SDT** är bunden till en XML-nod i dokumentets datalager. Standardvärdet ärDateTime

```csharp
public SdtDateStorageFormat DateStorageFormat { get; set; }
```

## Anmärkningar

Åtkomst till den här egendomen fungerar endast förDate SDT-typ.

För alla andra SDT-typer kommer undantag att inträffa.

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

* enum [SdtDateStorageFormat](../../sdtdatestorageformat/)
* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
