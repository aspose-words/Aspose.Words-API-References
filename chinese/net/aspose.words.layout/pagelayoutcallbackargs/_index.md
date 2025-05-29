---
title: PageLayoutCallbackArgs Class
linktitle: PageLayoutCallbackArgs
articleTitle: PageLayoutCallbackArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.PageLayoutCallbackArgs 类，实现高效的文档布局管理。强大的通知功能可增强您的工作流程。
type: docs
weight: 3810
url: /zh/net/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class

传入的参数[`Notify`](../ipagelayoutcallback/notify/)

要了解更多信息，请访问[转换为固定页面格式](https://docs.aspose.com/words/net/converting-to-fixed-page-format/)文档文章。

```csharp
public class PageLayoutCallbackArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.layout/pagelayoutcallbackargs/document/) { get; } | 获取文档。 |
| [Event](../../aspose.words.layout/pagelayoutcallbackargs/event/) { get; } | 获取事件。 |
| [PageIndex](../../aspose.words.layout/pagelayoutcallbackargs/pageindex/) { get; } | 获取与此事件相关的文档中页面的基于 0 的索引。 如果没有关联页面，或者页面在重排期间被删除，则返回负值。 |

## 例子

展示如何使用布局回调来跟踪布局变化。

```csharp
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// 当我们将文档保存为固定页面格式时通知我们
/// 并呈现一个页面，我们对该页面执行页面重排以将其呈现到本地文件系统中的图像上。
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
