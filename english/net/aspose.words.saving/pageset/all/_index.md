---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words for .NET
description: Access all document pages in their original order with PageSet All property. Streamline your workflow and enhance document management effortlessly!
type: docs
weight: 20
url: /net/aspose.words.saving/pageset/all/
---
## PageSet.All property

Gets a set with all the pages of the document in their original order.

```csharp
public static PageSet All { get; }
```

## Examples

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

* class [PageSet](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
