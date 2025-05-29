---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.HtmlOfficeMathOutputMode förbättrar OfficeMath-export till HTML, MHTML och EPUB för sömlös dokumentkonvertering.
type: docs
weight: 5850
url: /sv/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Anger hur Aspose.Words exporterar OfficeMath till HTML, MHTML och EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Image | `0` | OfficeMath konverteras till HTML enligt bilden som anges av &lt;img&gt;-taggen. |
| MathML | `1` | OfficeMath konverteras till HTML med MathML. |
| Text | `2` | OfficeMath konverteras till HTML som en sekvens av körningar som anges av &lt;span&gt;-taggar. |

## Exempel

Visar hur man anger hur man exporterar Microsoft OfficeMath-objekt till HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att avgöra hur sparoperationen hanterar OfficeMath-objekt.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.Image"
// kommer att rendera varje OfficeMath-objekt till en bild.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.MathML"
// kommer att konvertera varje OfficeMath-objekt till MathML.
// Ställer in egenskapen "OfficeMathOutputMode" till "HtmlOfficeMathOutputMode.Text"
// kommer att representera varje OfficeMath-formel med vanlig HTML-text.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">" +
                "<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" +
                    "<mi>i</mi>" +
                    "<mo>[+]</mo>" +
                    "<mi>b</mi>" +
                    "<mo>-</mo>" +
                    "<mi>c</mi>" +
                    "<mo>≥</mo>" +
                    ".*" +
                "</math>" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.True(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success);
        break;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
