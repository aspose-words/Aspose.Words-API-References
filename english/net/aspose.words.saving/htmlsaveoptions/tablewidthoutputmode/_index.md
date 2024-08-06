---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: Aspose.Words for .NET
description: HtmlSaveOptions TableWidthOutputMode property. Controls how table row and cell widths are exported to HTML MHTML or EPUB. Default value is All in C#.
type: docs
weight: 470
url: /net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is All.

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Remarks

In the HTML format, table, row and cell elements (**&lt;table&gt;**, **&lt;tr&gt;**, **&lt;th&gt;**, **&lt;td&gt;**) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.

When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).

Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode RelativeOnly or None so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.

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
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### See Also

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
