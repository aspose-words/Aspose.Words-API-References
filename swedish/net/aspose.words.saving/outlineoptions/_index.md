---
title: Class OutlineOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.OutlineOptions klass. Gör det möjligt att ange konturalternativ.
type: docs
weight: 5360
url: /sv/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

Gör det möjligt att ange konturalternativ.

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
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer om saknade dispositionsnivåer ska skapas eller inte när dokumentet exporteras. |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | Anger om konturer ska skapas för rubriker (stycken formaterade med rubrikstilar) i tabeller. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | Anger standardnivån i dokumentkonturen där Word-bokmärken ska visas. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | Anger hur många nivåer i dokumentkonturen som ska visas utökad när filen visas. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | Anger hur många nivåer av rubriker (stycken formaterade med rubrikstilar) som ska inkluderas i dokumentkonturen. |

### Exempel

Visar att bearbeta bokmärken i sidhuvuden/sidfötter i ett dokument som vi renderar till PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Ställ in "PageMode"-egenskapen till "PdfPageMode.UseOutlines" för att visa konturnavigeringsfönstret i utdata-PDF-filen.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Ställ in egenskapen "DefaultBookmarksOutlineLevel" till "1" för att visa alla
// bokmärken på den första nivån av konturen i utdata-PDF.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.None" till
// exportera inte några bokmärken som finns i sidhuvuden/sidfötter.
// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.First" till
// exportera endast bokmärken i det första avsnittets sidhuvud/sidfötter.
// Ställ in egenskapen "HeaderFooterBookmarksExportMode" till "HeaderFooterBookmarksExportMode.All" till
// exportera bokmärken som finns i alla sidhuvuden/sidfötter.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


