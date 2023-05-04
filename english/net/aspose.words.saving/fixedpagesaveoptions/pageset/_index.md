---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: FixedPageSaveOptions PageSet property. Gets or sets the pages to render. Default is all the pages in the document in C#.
type: docs
weight: 70
url: /net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Gets or sets the pages to render. Default is all the pages in the document.

```csharp
public PageSet PageSet { get; set; }
```

## Examples

Shows how to extract pages based on exact page indices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add five pages to the document.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Use the "PageSet" property to select a set of the document's pages to save to output XPS.
// In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

Shows how to convert only some of the pages in a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
    // to modify how that method converts the document to .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Set the "PageIndex" to "1" to render a portion of the document starting from the second page.
    options.PageSet = new PageSet(1);

    // This document will contain one page starting from page two, which will only contain the second page.
    doc.Save(stream, options);
}
```

Shows how to export Odd pages from the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Below are three PageSet properties that we can use to filter out a set of pages from
// our document to save in an output PDF document based on the parity of their page numbers.
// 1 -  Save only the even-numbered pages:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 -  Save only the odd-numbered pages:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 -  Save every page:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### See Also

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* namespace [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* assembly [Aspose.Words](../../../)
