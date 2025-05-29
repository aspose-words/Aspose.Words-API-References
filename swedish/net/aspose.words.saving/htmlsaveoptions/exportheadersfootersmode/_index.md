---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportHeadersFootersMode optimerar sidhuvud- och sidfotsutdata för HTML-, MHTML- och EPUB-format. Maximera presentationen av ditt dokument!
type: docs
weight: 160
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Anger hur sidhuvuden och sidfot visas som HTML, MHTML eller EPUB. Standardvärdet ärPerSection för HTML/MHTML ochNone för EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Anmärkningar

Det är svårt att meningsfullt mata ut sidhuvuden och sidfot till HTML eftersom HTML inte är paginerad.

När den här egendomen ärPerSection, Aspose.Words exports endast primära sidhuvuden och sidfot i början och slutet av varje avsnitt.

När det ärFirstSectionHeaderLastSectionFooter endast den första primära sidhuvudet och den sista primära sidfoten (inklusive länkad till föregående) exporteras.

Du kan inaktivera export av sidhuvuden och sidfot helt och hållet genom att ställa in egenskapen tillNone.

## Exempel

Visar hur man utelämnar sidhuvuden/sidfot när man sparar ett dokument som HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Detta dokument innehåller sidhuvuden och sidfot. Vi kan komma åt dem via samlingen "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Format som .html delar inte upp dokumentet i sidor, så sidhuvuden/sidfot fungerar inte på samma sätt
// de skulle göra det när vi öppnade dokumentet som en .docx med Microsoft Word.
// Om vi konverterar ett dokument med sidhuvuden/sidfötter till html, kommer konverteringen att assimilera sidhuvudena/sidfötterna till brödtexten.
// Vi kan använda ett SaveOptions-objekt för att utelämna sidhuvuden/sidfot vid konvertering till html.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Öppna vårt sparade dokument och kontrollera att det inte innehåller rubrikens text
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Se även

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
