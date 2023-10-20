---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportHeadersFootersMode fast egendom. Anger hur sidhuvuden och sidfötter matas ut till HTML MHTML eller EPUB. Standardvärdet ärPerSection för HTML/MHTML ochNone för EPUB i C#.
type: docs
weight: 160
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Anger hur sidhuvuden och sidfötter matas ut till HTML, MHTML eller EPUB. Standardvärdet ärPerSection för HTML/MHTML ochNone för EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Anmärkningar

Det är svårt att meningsfullt mata ut sidhuvuden och sidfötter till HTML eftersom HTML inte är paginerad.

När denna fastighet ärPerSection, Aspose.Words exports endast primära sidhuvuden och sidfötter i början och slutet av varje avsnitt.

När det ärFirstSectionHeaderLastSectionFooter endast den första primära sidhuvudet och den sista primära sidfoten (inklusive länkad till föregående) exporteras.

Du kan inaktivera export av sidhuvuden och sidfötter helt och hållet genom att ställa in denna egenskap tillNone.

## Exempel

Visar hur du utelämnar sidhuvuden/sidfötter när du sparar ett dokument i HTML.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Detta dokument innehåller sidhuvuden och sidfötter. Vi kan komma åt dem via samlingen "HeadersFooters".
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Format som .html delar inte upp dokumentet i sidor, så sidhuvuden/sidfötter fungerar inte på samma sätt
// skulle de göra när vi öppnar dokumentet som en .docx med Microsoft Word.
// Om vi konverterar ett dokument med sidhuvuden/sidfötter till html, kommer konverteringen att assimilera sidhuvuden/sidfötter till brödtext.
// Vi kan använda ett SaveOptions-objekt för att utelämna sidhuvuden/sidfötter när vi konverterar till html.
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
