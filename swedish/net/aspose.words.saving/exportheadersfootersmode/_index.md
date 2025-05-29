---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words ExportHeadersFootersMode-enum för sömlös export av sidhuvud och sidfot i HTML, MHTML eller EPUB. Optimera din dokumentkonvertering idag!
type: docs
weight: 5750
url: /sv/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Anger hur sidhuvuden och sidfot exporteras till HTML, MHTML eller EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Sidhuvuden och sidfot exporteras inte. |
| PerSection | `1` | Primära sidhuvuden och sidfot exporteras i början och slutet av varje avsnitt. |
| FirstSectionHeaderLastSectionFooter | `2` | Det primära sidhuvudet för det första avsnittet exporteras i början av dokumentet och det primära sidfoten finns i slutet. |
| FirstPageHeaderFooterPerSection | `3` | Sidhuvud och sidfot på första sidan exporteras i början och slutet av varje avsnitt. |

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
