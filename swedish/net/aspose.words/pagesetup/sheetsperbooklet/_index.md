---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup SheetsPerBooklet för att enkelt hantera antalet häften, vilket förbättrar dokumentlayouten och utskriftseffektiviteten.
type: docs
weight: 400
url: /sv/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Returnerar eller anger antalet sidor som ska inkluderas i varje häfte.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Exempel

Visar hur man konfigurerar ett dokument som kan skrivas ut som en bokvikning.

```csharp
Document doc = new Document();

// Infoga text som sträcker sig över 16 sidor.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurera den första sektionens "PageSetup"-egenskap för att skriva ut dokumentet i form av en bokvikning.
// När vi skriver ut detta dokument på båda sidor kan vi ta sidorna och stapla dem
// och vik dem alla på mitten samtidigt. Innehållet i dokumentet kommer att radas upp till en bokvikning.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Vi kan bara ange antalet ark i multiplar av 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
