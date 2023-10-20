---
title: PageInfo Class
linktitle: PageInfo
articleTitle: PageInfo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Rendering.PageInfo 班级. 表示有关特定文档页面的信息 在 C#.
type: docs
weight: 4570
url: /zh/net/aspose.words.rendering/pageinfo/
---
## PageInfo class

表示有关特定文档页面的信息。

要了解更多信息，请访问[渲染](https://docs.aspose.com/words/net/rendering/)文档文章。

```csharp
public class PageInfo
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Colored](../../aspose.words.rendering/pageinfo/colored/) { get; } | 返回`真的`如果页面包含彩色内容。 |
| [HeightInPoints](../../aspose.words.rendering/pageinfo/heightinpoints/) { get; } | 获取页面的高度（以磅为单位）。 |
| [Landscape](../../aspose.words.rendering/pageinfo/landscape/) { get; } | 返回`真的`如果文档中为此页面指定的页面方向是横向。 |
| [PaperSize](../../aspose.words.rendering/pageinfo/papersize/) { get; } | 获取纸张尺寸作为枚举。 |
| [PaperTray](../../aspose.words.rendering/pageinfo/papertray/) { get; } | 获取文档中指定的该页的纸盘 (bin)。 该值是特定于实现（打印机）的。 |
| [SizeInPoints](../../aspose.words.rendering/pageinfo/sizeinpoints/) { get; } | 获取页面大小（以磅为单位）。 |
| [WidthInPoints](../../aspose.words.rendering/pageinfo/widthinpoints/) { get; } | 获取页面的宽度（以磅为单位）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetDotNetPaperSize](../../aspose.words.rendering/pageinfo/getdotnetpapersize/)(*PaperSizeCollection*) | 获取PaperSize适合打印 由此表示的页面的对象`PageInfo`. |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels)(*float, float*) | 计算指定缩放系数和分辨率的页面大小（以像素为单位）。 |
| [GetSizeInPixels](../../aspose.words.rendering/pageinfo/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | 计算指定缩放系数和分辨率的页面大小（以像素为单位）。 |
| [GetSpecifiedPrinterPaperSource](../../aspose.words.rendering/pageinfo/getspecifiedprinterpapersource/)(*PaperSourceCollection, PaperSource*) | 获取PaperSource适合打印 由此表示的页面的对象`PageInfo`. |

## 评论

该对象返回的页面宽度和高度表示页面的“最终”尺寸，例如它们 已经旋转到正确的方向。

## 例子

演示如何打印 Word 文档中每个页面的页面大小和方向信息。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 第一部分有 2 页。我们将为每台打印机分配一个不同的打印机纸盘，
// 其编号将与一种纸张来源相匹配。这些来源及其种类会有所不同
// 取决于安装的打印机驱动程序。
PrinterSettings.PaperSourceCollection paperSources = new PrinterSettings().PaperSources;

doc.FirstSection.PageSetup.FirstPageTray = paperSources[0].RawKind;
doc.FirstSection.PageSetup.OtherPagesTray = paperSources[1].RawKind;

Console.WriteLine("Document \"{0}\" contains {1} pages.", doc.OriginalFileName, doc.PageCount);

float scale = 1.0f;
float dpi = 96;

for (int i = 0; i < doc.PageCount; i++)
{
    // 每个页面都有一个 PageInfo 对象，其索引是相应页面的编号。
    PageInfo pageInfo = doc.GetPageInfo(i);

    // 打印页面的方向和尺寸。
    Console.WriteLine($"Page {i + 1}:");
    Console.WriteLine($"\tOrientation:\t{(pageInfo.Landscape ? "Landscape" : "Portrait")}");
    Console.WriteLine($"\tPaper size:\t\t{pageInfo.PaperSize} ({pageInfo.WidthInPoints:F0}x{pageInfo.HeightInPoints:F0}pt)");
    Console.WriteLine($"\tSize in points:\t{pageInfo.SizeInPoints}");
    Console.WriteLine($"\tSize in pixels:\t{pageInfo.GetSizeInPixels(1.0f, 96)} at {scale * 100}% scale, {dpi} dpi");

    // 打印源托盘信息。
    Console.WriteLine($"\tTray:\t{pageInfo.PaperTray}");
    PaperSource source = pageInfo.GetSpecifiedPrinterPaperSource(paperSources, paperSources[0]);
    Console.WriteLine($"\tSuitable print source:\t{source.SourceName}, kind: {source.Kind}");
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
