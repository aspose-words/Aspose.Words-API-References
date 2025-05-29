---
title: IPageLayoutCallback Interface
linktitle: IPageLayoutCallback
articleTitle: IPageLayoutCallback
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Layout.IPageLayoutCallback 接口自定义文档布局。使用您自己的方法增强渲染效果，以获得最佳效果。
type: docs
weight: 3760
url: /zh/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

如果您希望在构建和渲染页面布局模型期间调用自己的自定义方法，请实现此接口。

```csharp
public interface IPageLayoutCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(*[PageLayoutCallbackArgs](../pagelayoutcallbackargs/)*) | 调用此函数来通知布局构建和渲染进度。 |

## 评论

此接口的主要用途是允许应用程序代码中止构建过程。

可以在文档开始时仅为几页构建页面布局模型，然后中止进程并仅渲染已构建的内容。

但请注意，如果过程已经完成，渲染结果可能与每个页面渲染的结果不匹配。

此技术可能不适用于每个文档，或者可能完全失败。

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

* property [Callback](../layoutoptions/callback/)
* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
