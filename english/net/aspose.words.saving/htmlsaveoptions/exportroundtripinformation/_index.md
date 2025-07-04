---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words for .NET
description: Discover HtmlSaveOptions' ExportRoundtripInformation property to control roundtrip data in HTML, MHTML, and EPUB formats. Optimize your exports today!
type: docs
weight: 240
url: /net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is `true` for HTML and `false` for MHTML and EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Remarks

Saving of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [`Document`](../../../aspose.words/document/) object.

When `true`, the roundtrip information is exported as -aw-* CSS properties of the corresponding HTML elements.

When `false`, causes no roundtrip information to be output into produced files.

## Examples

Shows how to preserve hidden elements when converting to .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
// or footnotes will be either removed or converted to plain text and effectively be lost.
// Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.

// When we save the document to HTML, we can pass a SaveOptions object to determine
// how the saving operation will export document elements that HTML does not support or use,
// such as hidden bookmarks and original shape positions.
// If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
// If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
// We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
// as they could be of use once again.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.That(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"), Is.True);
    Assert.That(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"), Is.True);

    Assert.That(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"), Is.True);

    Assert.That(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"), Is.True);

    Assert.That(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"), Is.True);

    Assert.That(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"), Is.True);

    Assert.That(doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage), Is.EqualTo(1));
}
else
{
    Assert.That(outDocContents.Contains("<div style=\"clear:both\">"), Is.True);
    Assert.That(outDocContents.Contains("<span>&#xa0;</span>"), Is.True);

    Assert.That(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"), Is.True);

    Assert.That(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"), Is.True);

    Assert.That(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"), Is.True);

    Assert.That(outDocContents.Contains(
        "<span>Page number 1</span>"), Is.True);

    Assert.That(doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage), Is.EqualTo(0));
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
