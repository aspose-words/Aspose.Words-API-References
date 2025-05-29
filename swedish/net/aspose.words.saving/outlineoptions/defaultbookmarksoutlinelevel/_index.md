---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen DefaultBookmarksOutlineLevel förbättrar dina Word-dokument genom att optimera bokmärkenas synlighet i dispositionen. Öka produktiviteten idag!
type: docs
weight: 50
url: /sv/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Anger standardnivån i dokumentdispositionen där Word-bokmärken ska visas.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Anmärkningar

Nivå för individuella bokmärken kan anges med hjälp av[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) egendom.

Ange 0 så visas inte Word-bokmärken i dokumentdispositionen. Ange 1 så visas Word-bokmärken i dokumentdispositionen på nivå 1; 2 för nivå 2 och så vidare.

Standardvärdet är 0. Giltigt intervall är 0 till 9.

## Exempel

Visar att bearbeta bokmärken i sidhuvuden/sidfötter i ett dokument som vi renderar till PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in egenskapen "PageMode" till "PdfPageMode.UseOutlines" för att visa dispositionsnavigeringsfönstret i den utgående PDF-filen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Sätt egenskapen "DefaultBookmarksOutlineLevel" till "1" för att visa alla
// bokmärken på den första nivån av dispositionen i den utgående PDF-filen.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.None"
// exportera inte några bokmärken som finns inuti sidhuvuden/sidfoten.
// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.First" till
// exportera endast bokmärken i den första sektionens sidhuvud/sidfot.
// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.All" till
// exportera bokmärken som finns i alla sidhuvuden/sidfot.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Se även

* class [OutlineOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
