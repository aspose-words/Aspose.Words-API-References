---
title: PageInfo.Landscape
linktitle: Landscape
articleTitle: Landscape
second_title: 用于 .NET 的 Aspose.Words
description: PageInfo Landscape 财产. 返回真的如果文档中为此页面指定的页面方向是横向 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.rendering/pageinfo/landscape/
---
## PageInfo.Landscape property

返回`真的`如果文档中为此页面指定的页面方向是横向。

```csharp
public bool Landscape { get; }
```

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

演示如何自定义 Aspose.Words 文档的打印。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// 打印时选择适当的纸张尺寸、方向和纸盘。
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// 根据用户选择初始化要打印的页面范围。
    /// </summary>
    protected override void OnBeginPrint(PrintEventArgs e)
    {
        base.OnBeginPrint(e);

        switch (PrinterSettings.PrintRange)
        {
            case System.Drawing.Printing.PrintRange.AllPages:
                mCurrentPage = 1;
                mPageTo = mDocument.PageCount;
                break;
            case System.Drawing.Printing.PrintRange.SomePages:
                mCurrentPage = PrinterSettings.FromPage;
                mPageTo = PrinterSettings.ToPage;
                break;
            default:
                throw new InvalidOperationException("Unsupported print range.");
        }
    }

    /// <summary>
     /// 在打印每页之前调用。
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // 单个 Microsoft Word 文档可以有多个部分，指定不同大小的页面，
         // 方向和纸盘。 .NET 打印框架之前调用此代码
        // 每一页都会被打印，这让我们有机会指定如何打印当前页面。
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word 将每个部分的纸张来源（打印机托盘）存储为打印机特定值。
        // 要获取正确的纸盘值，您需要使用打印机应返回的“RawKind”属性。
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// 调用每个页面来渲染它以进行打印。
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Aspose.Words 渲染引擎创建一个从纸张原点 (x = 0, y = 0) 绘制的页面。
        // 打印机中会有一个硬边距，它将渲染每一页。我们需要用硬利润来抵消。
        float hardOffsetX, hardOffsetY;

        // 下面是设置硬边距的两种方法。
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - 通过“PageSettings”属性。
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - 如果“PageSettings”属性不可用，则使用我们自己的值。
            hardOffsetX = 20;
            hardOffsetY = 20;
        }

        mDocument.RenderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

        mCurrentPage++;
        e.HasMorePages = mCurrentPage <= mPageTo;
    }

    private readonly Document mDocument;
    private int mCurrentPage;
    private int mPageTo;
}
```

### 也可以看看

* class [PageInfo](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
