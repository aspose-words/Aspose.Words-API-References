---
title: PageInfo.PaperSize
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words for .NET
description: Discover the PageInfo PaperSize property to easily retrieve paper sizes as an enumeration. Enhance your printing capabilities today!
type: docs
weight: 40
url: /net/aspose.words.rendering/pageinfo/papersize/
---
## PageInfo.PaperSize property

Gets the paper size as enumeration.

```csharp
public PaperSize PaperSize { get; }
```

## Examples

Shows how to print page size and orientation information for every page in a Word document.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// The first section has 2 pages. We will assign a different printer paper tray to each one,
// whose number will match a kind of paper source. These sources and their Kinds will vary
// depending on the installed printer driver.
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // Each page has a PageInfo object, whose index is the respective page's number.
    PageInfo pageInfo = doc.GetPageInfo(i);

    // Print the page's orientation and dimensions.
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // Print the source tray information.
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### See Also

* enum [PaperSize](../../../aspose.words/papersize/)
* class [PageInfo](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
