---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfPageMode-enum för anpassningsbara PDF-visningsalternativ, vilket förbättrar användarupplevelsen i alla PDF-läsare. Optimera dina dokument idag!
type: docs
weight: 6300
url: /sv/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

Anger hur PDF-dokumentet ska visas när det öppnas i PDF-läsaren.

```csharp
public enum PdfPageMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| UseNone | `0` | Varken dokumentets disposition eller miniatyrbilder är synliga. |
| UseOutlines | `1` | Dokumentets disposition är synlig. Observera att om det inte finns några dispositioner i PDF-dokumentet kommer dispositionsnavigeringsfönstret ändå inte att synas. |
| UseThumbs | `2` | Miniatyrbilder är synliga. |
| FullScreen | `3` | Helskärmsläge, utan menyrad, fönsterkontroller eller något annat synligt fönster. |
| UseOC | `4` | Panelen för valfri innehållsgrupp är synlig. |
| UseAttachments | `5` | Panelen för bilagor är synlig. |

## Exempel

Visar hur man ställer in instruktioner som vissa PDF-läsare ska följa när ett utdatadokument öppnas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "PageMode" till "PdfPageMode.FullScreen" för att få PDF-läsaren att öppna den sparade filen
// dokument i helskärmsläge, vilket tar över skärmens visning och inte har några synliga kontroller.
// Ställ in egenskapen "PageMode" till "PdfPageMode.UseThumbs" för att få PDF-läsaren att visa en separat panel
// med en miniatyrbild för varje sida i dokumentet.
// Ställ in egenskapen "PageMode" till "PdfPageMode.UseOC" för att få PDF-läsaren att visa en separat panel
// som låter oss arbeta med alla lager som finns i dokumentet.
// Ställ in egenskapen "PageMode" till "PdfPageMode.UseOutlines" för att hämta PDF-läsaren
// även för att visa konturen, om möjligt.
// Ställ in egenskapen "PageMode" till "PdfPageMode.UseNone" för att få PDF-läsaren att bara visa själva dokumentet.
// Ställ in egenskapen "PageMode" till "PdfPageMode.UseAttachments" för att göra panelen med bilagor synlig.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

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
