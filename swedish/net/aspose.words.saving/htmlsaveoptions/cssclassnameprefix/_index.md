---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions CssClassNamePrefix för att enkelt anpassa CSS-klassnamn med ett unikt prefix, vilket förbättrar din webbdesigns konsekvens.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Anger ett prefix som läggs till alla CSS-klassnamn. Standardvärdet är en tom sträng och genererade CSS-klassnamn har inget gemensamt prefix.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | Värdet är inte tomt och är inte en giltig CSS-identifierare. |

## Anmärkningar

Om detta värde inte är tomt kommer alla CSS-klasser som genereras av Aspose.Words att börja med det angivna prefixet. . Detta kan vara användbart om du till exempel lägger till anpassad CSS i genererade dokument och vill förhindra namnkonflikter i class .

Om värdet inte är`null` eller tom, måste det vara en giltig CSS-identifierare.

## Exempel

Visar hur man sparar ett dokument till HTML och lägger till ett prefix till alla dess CSS-klassnamn.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
