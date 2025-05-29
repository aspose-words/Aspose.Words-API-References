---
title: HtmlFixedSaveOptions.PageHorizontalAlignment
linktitle: PageHorizontalAlignment
articleTitle: PageHorizontalAlignment
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlFixedSaveOptions PageHorizontalAlignment för att enkelt kontrollera sidjustering i HTML-dokument. Standardinställningen är Centrerad för optimal presentation.
type: docs
weight: 120
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/
---
## HtmlFixedSaveOptions.PageHorizontalAlignment property

Anger den horisontella justeringen av sidor i ett HTML-dokument. Standardvärdet ärCenter .

```csharp
public HtmlFixedPageHorizontalAlignment PageHorizontalAlignment { get; set; }
```

## Exempel

Visar hur man ställer in den horisontella justeringen av sidor när man sparar ett dokument som HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### Se även

* enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
