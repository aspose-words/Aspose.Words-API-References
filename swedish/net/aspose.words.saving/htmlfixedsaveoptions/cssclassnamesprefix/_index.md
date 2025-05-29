---
title: HtmlFixedSaveOptions.CssClassNamesPrefix
linktitle: CssClassNamesPrefix
articleTitle: CssClassNamesPrefix
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlFixedSaveOptions CssClassNamesPrefix förbättrar din stil genom att lägga till ett anpassningsbart prefix till alla klassnamn i din style.css.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/
---
## HtmlFixedSaveOptions.CssClassNamesPrefix property

Anger prefix som läggs till alla klassnamn i style.css-filen. Standardvärdet är`"åh"` .

```csharp
public string CssClassNamesPrefix { get; set; }
```

## Exempel

Visar hur man placerar CSS i en separat fil och lägger till ett prefix till alla dess CSS-klassnamn.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
