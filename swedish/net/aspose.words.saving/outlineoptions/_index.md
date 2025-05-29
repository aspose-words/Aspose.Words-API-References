---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Saving.OutlineOptions för att anpassa dokumentets dispositionsinställningar för förbättrad organisation och tydlighet.
type: docs
weight: 6140
url: /sv/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Gör det möjligt att ange dispositionsalternativ.

För att lära dig mer, besök[Spara ett dokument](https://docs.aspose.com/words/net/save-a-document/) dokumentationsartikel.

```csharp
public class OutlineOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | Gör det möjligt att ange individuella bokmärkens konturnivå. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Hämtar eller anger ett värde som avgör om saknade dispositionsnivåer ska skapas när dokumentet exporteras. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Anger om dispositioner ska skapas för rubriker (stycken formaterade med rubrikformat) inuti tabeller. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Anger standardnivån i dokumentdispositionen där Word-bokmärken ska visas. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Anger hur många nivåer i dokumentdispositionen som ska visas expanderad när filen visas. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Anger hur många nivåer av rubriker (stycken formaterade med rubrikformaten) som ska inkluderas i dokumentdispositionen. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
