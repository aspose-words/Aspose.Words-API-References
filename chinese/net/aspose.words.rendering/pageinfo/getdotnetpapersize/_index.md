---
title: PageInfo.GetDotNetPaperSize
second_title: Aspose.Words for .NET API 参考
description: PageInfo 方法. 获取PaperSize适合打印 由此表示的页面的对象PageInfo.
type: docs
weight: 80
url: /zh/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

获取PaperSize适合打印 由此表示的页面的对象[`PageInfo`](../).

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | 可用的纸张尺寸。 |

### 返回值

可以在 .NET 打印框架中使用的对象来指定纸张尺寸。

### 例子

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
* 命名空间 [Aspose.Words.Rendering](../../pageinfo/)
* 部件 [Aspose.Words](../../../)


