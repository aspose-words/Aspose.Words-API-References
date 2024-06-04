---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.PageInfo class. Represents information about a particular document page in C#.
type: docs
weight: 4800
url: /net/aspose.words.rendering/pageinfo/
---
## PageInfo class

Represents information about a particular document page.

To learn more, visit the [Rendering](https://docs.aspose.com/words/net/rendering/) documentation article.

```csharp
public class PageInfo
```

## Properties

| Name | Description |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | Returns `true` if the page contains colored content. |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | Gets the height of the page in points. |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | Returns `true` if the page orientation specified in the document for this page is landscape. |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | Gets the paper size as enumeration. |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | Gets the paper tray (bin) for this page as specified in the document. The value is implementation (printer) specific. |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | Gets the page size in points. |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | Gets the width of the page in points. |

## Methods

| Name | Description |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | Gets the PaperSize object suitable for printing the page represented by this `PageInfo`. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | Gets the PaperSource object suitable for printing the page represented by this `PageInfo`. |

## Remarks

The page width and height returned by this object represent the "final" size of the page e.g. they are already rotated to the correct orientation.

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

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
