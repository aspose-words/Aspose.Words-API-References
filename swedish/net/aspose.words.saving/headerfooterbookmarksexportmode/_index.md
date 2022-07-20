---
title: HeaderFooterBookmarksExportMode
second_title: Aspose.Words för .NET API Referens
description: Anger hur bokmärken i sidhuvuden/sidfötter exporteras.
type: docs
weight: 4790
url: /sv/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Anger hur bokmärken i sidhuvuden/sidfötter exporteras.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Bokmärken i sidhuvuden/sidfötter exporteras inte. |
| First | `1` | Endast bokmärke i första sidhuvudet/sidfoten i avsnittet exporteras. |
| All | `2` | Bokmärken i alla sidhuvuden/sidfötter exporteras. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->