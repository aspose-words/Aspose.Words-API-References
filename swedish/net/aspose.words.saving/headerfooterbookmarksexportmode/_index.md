---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.HeaderFooterBookmarksExportMode förbättrar bokmärkesexport i sidhuvuden och sidfötter för smidig dokumenthantering.
type: docs
weight: 5800
url: /sv/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Anger hur bokmärken i sidhuvuden/sidfot exporteras.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Bokmärken i sidhuvuden/sidfot exporteras inte. |
| First | `1` | Endast bokmärket i första sidhuvudet/sidfoten i avsnittet exporteras. |
| All | `2` | Bokmärken i alla sidhuvuden/sidfot exporteras. |

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
