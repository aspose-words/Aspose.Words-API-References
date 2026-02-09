---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: Aspose.Words for .NET
description: Discover how Aspose.Words' TxtExportHeadersFootersMode enum enhances plain text exports by customizing header and footer handling for optimal results.
type: docs
weight: 6510
url: /net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Specifies the way headers and footers are exported to plain text format.

```csharp
public enum TxtExportHeadersFootersMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No headers and footers are exported. |
| PrimaryOnly | `1` | Only primary headers and footers are exported at the beginning and end of each section. |
| AllAtEnd | `2` | All headers and footers are placed after all section bodies at the very end of a document. |

## Examples

Shows how to specify how to export headers and footers to plain text format.

```csharp
Document doc = new Document();

// Insert even and primary headers/footers into the document.
// The primary header/footers will override the even headers/footers.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Insert pages to display these headers and footers.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.None"
// to not export any headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.PrimaryOnly"
// to only export primary headers/footers.
// Set the "ExportHeadersFootersMode" property to "TxtExportHeadersFootersMode.AllAtEnd"
// to place all headers and footers for all section bodies at the end of the document.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.That(docText, Is.EqualTo($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}"));
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.That(docText, Is.EqualTo($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}"));
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.That(docText, Is.EqualTo($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}"));
        break;
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
