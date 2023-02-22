---
title: Enum ExportHeadersFootersMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.ExportHeadersFootersMode uppräkning. Anger hur sidhuvuden och sidfötter exporteras till HTML MHTML eller EPUB.
type: docs
weight: 4740
url: /sv/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB.

```csharp
public enum ExportHeadersFootersMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Sidhuvuden och sidfötter exporteras inte. |
| PerSection | `1` | Primära sidhuvuden och sidfötter exporteras i början och slutet av varje avsnitt. |
| FirstSectionHeaderLastSectionFooter | `2` | Primär sidhuvud för det första avsnittet exporteras i början av dokumentet och primär sidfot är i slutet. |
| FirstPageHeaderFooterPerSection | `3` | Första sidans sidhuvud och sidfot exporteras i början och slutet av varje avsnitt. |

### Exempel

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

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


