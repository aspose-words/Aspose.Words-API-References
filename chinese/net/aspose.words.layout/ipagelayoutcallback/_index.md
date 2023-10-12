---
title: Interface IPageLayoutCallback
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Layout.IPageLayoutCallback 界面. 如果您想在构建和渲染页面布局模型期间调用自己的自定义方法请实现此接口
type: docs
weight: 3310
url: /zh/net/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface

如果您想在构建和渲染页面布局模型期间调用自己的自定义方法，请实现此接口。

```csharp
public interface IPageLayoutCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Notify](../../aspose.words.layout/ipagelayoutcallback/notify/)(PageLayoutCallbackArgs) | 调用此函数以通知布局构建和渲染进度。 |

### 评论

此接口的主要用途是允许应用程序代码中止构建过程。

可以在文档开头仅构建几个页面的页面布局模型，然后中止进程并仅渲染已经构建的内容。

但请注意，如果进程已完成，渲染结果可能与每个页面渲染的结果不匹配。

此技术可能不适用于每个文档，或者可能完全失败。

### 例子

展示如何使用布局回调跟踪布局更改。

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
/// 并渲染一个页面，我们将其执行页面回流到本地文件系统中的图像。
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


