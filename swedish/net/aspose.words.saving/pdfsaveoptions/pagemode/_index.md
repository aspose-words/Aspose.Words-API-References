---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen PdfSaveOptions PageMode förbättrar din PDF-visningsupplevelse genom att anpassa dokumentvisningen i valfri PDF-läsare.
type: docs
weight: 260
url: /sv/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Anger hur PDF-dokumentet ska visas när det öppnas i en PDF-läsare.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Anmärkningar

Standardvärdet ärUseOutlines .

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

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
