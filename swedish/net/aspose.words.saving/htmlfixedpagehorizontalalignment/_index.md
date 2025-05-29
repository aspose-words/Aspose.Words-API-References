---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.HtmlFixedPageHorizontalAlignment-enum för exakt kontroll över sidjusteringen i dina HTML-dokument. Förbättra din dokumentformatering idag!
type: docs
weight: 5820
url: /sv/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Anger den horisontella justeringen för sidor i HTML-utdatadokumentet.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Justera sidorna åt vänster. |
| Center | `1` | Centrera sidorna. Detta är standardvärdet. |
| Right | `2` | Justera sidorna åt höger. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
