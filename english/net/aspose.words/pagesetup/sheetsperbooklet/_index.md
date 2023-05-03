---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
second_title: Aspose.Words for .NET API Reference
description: PageSetup SheetsPerBooklet property. Returns or sets the number of pages to be included in each booklet in C#.
type: docs
weight: 400
url: /net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Returns or sets the number of pages to be included in each booklet.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Examples

Shows how to configure a document that can be printed as a book fold.

```csharp
Document doc = new Document();

// Insert text that spans 16 pages.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configure the first section's "PageSetup" property to print the document in the form of a book fold.
// When we print this document on both sides, we can take the pages to stack them
// and fold them all down the middle at once. The contents of the document will line up into a book fold.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// We can only specify the number of sheets in multiples of 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### See Also

* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
