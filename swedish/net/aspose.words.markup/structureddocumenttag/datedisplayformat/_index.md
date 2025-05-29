---
title: StructuredDocumentTag.DateDisplayFormat
linktitle: DateDisplayFormat
articleTitle: DateDisplayFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DateDisplayFormat i StructuredDocumentTag för att enkelt anpassa datumvisningsformat. Förbättra ditt dokuments tydlighet och attraktionskraft!
type: docs
weight: 90
url: /sv/net/aspose.words.markup/structureddocumenttag/datedisplayformat/
---
## StructuredDocumentTag.DateDisplayFormat property

Sträng som representerar formatet i vilket datum visas.

```csharp
public string DateDisplayFormat { get; set; }
```

## Anmärkningar

Kan inte vara`null`.

Datumet för engelska (USA) är "mm/dd/åååå"

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

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
