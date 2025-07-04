---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words for .NET
description: Discover how Aspose.Words.Saving.HtmlOfficeMathOutputMode enhances OfficeMath export to HTML, MHTML, and EPUB for seamless document conversion.
type: docs
weight: 5840
url: /net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Image | `0` | OfficeMath is converted to HTML as image specified by &lt;img&gt; tag. |
| MathML | `1` | OfficeMath is converted to HTML using MathML. |
| Text | `2` | OfficeMath is converted to HTML as sequence of runs specified by &lt;span&gt; tags. |

## Examples

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation handles OfficeMath objects.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
// will render each OfficeMath object into an image.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
// will convert each OfficeMath object into MathML.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
// will represent each OfficeMath formula using plain HTML text.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.That(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success, Is.True);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.That(Regex.Match(outDocContents,
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
            "</p>").Success, Is.True);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.That(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success, Is.True);
        break;
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
