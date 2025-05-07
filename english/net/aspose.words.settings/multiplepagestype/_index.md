---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Settings.MultiplePagesType enum for efficient document printing options. Optimize your workflow with flexible printing settings!
type: docs
weight: 6700
url: /net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Specifies how document is printed out.

```csharp
public enum MultiplePagesType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Normal | `0` | Normal printing, no multiple pages specified. |
| MirrorMargins | `1` | Swaps left and right margins on facing pages. |
| TwoPagesPerSheet | `2` | Prints two pages per sheet. |
| BookFoldPrinting | `3` | Specifies whether to print the document as a book fold. |
| BookFoldPrintingReverse | `4` | Specifies whether to print the document as a reverse book fold. |
| Default | `0` | Default value is Normal |

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

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
