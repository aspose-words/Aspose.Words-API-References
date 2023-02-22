---
title: ExportTocPageNumbers
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Specifies whether to write page numbers to table of contents when saving HTML MHTML and EPUB. Default value is false in C#.
type: docs
weight: 280
url: /net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is `false`.

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Examples

Shows how to display page numbers when saving a document with a table of contents to .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
// style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
// and the page number that contains the heading on the right.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// HTML documents do not have pages. If we save this document to HTML,
// the page numbers that our TOC displays will have no meaning.
// When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
// If we set the "ExportTocPageNumbers" flag to "true",
// each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
// If we set the "ExportTocPageNumbers" flag to "false",
// the save operation will omit both the separator and page number and leave the heading for each entry intact.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
