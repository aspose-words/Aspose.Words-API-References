---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.HtmlElementSizeOutputMode. Control element sizes for optimal HTML, MHTML, and EPUB exports. Enhance your document formatting!
type: docs
weight: 5870
url: /net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.

```csharp
public enum HtmlElementSizeOutputMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| All | `0` | All element sizes, both in absolute and relative units, specified in the document are exported. |
| RelativeOnly | `1` | Element sizes are exported only if they are specified in relative units in the document. Fixed sizes are not exported in this mode. Visual agents will calculate missing sizes to make document layout more natural. |
| None | `2` | Element sizes are not exported. Visual agents will build layout automatically according to relationship between elements. |

## Examples

Shows how to preserve negative indents in the output .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a table with a negative indent, which will push it to the left past the left page boundary.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Insert a table with a positive indent, which will push the table to the right.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// When we save a document to HTML, Aspose.Words will only preserve negative indents
// such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
// in a SaveOptions object that we will pass to "true".
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.That(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"), Is.True);
    Assert.That(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"), Is.True);
}
else
{
    Assert.That(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"), Is.True);
    Assert.That(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"), Is.True);
}
```

### See Also

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
