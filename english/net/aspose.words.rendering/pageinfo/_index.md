---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Rendering.PageInfo class, which provides essential details about each document page, enhancing your document rendering experience.
type: docs
weight: 5400
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

### See Also

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
