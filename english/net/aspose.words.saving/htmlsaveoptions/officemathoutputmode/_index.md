---
title: HtmlSaveOptions.OfficeMathOutputMode
linktitle: OfficeMathOutputMode
articleTitle: OfficeMathOutputMode
second_title: Aspose.Words for .NET
description: Discover HtmlSaveOptions' OfficeMathOutputMode for optimal HTML, MHTML, or EPUB exports. Customize OfficeMath object output with ease!
type: docs
weight: 400
url: /net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is Image.

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

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

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
