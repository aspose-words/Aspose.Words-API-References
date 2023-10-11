---
title: Enum PageLayoutEvent
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Layout.PageLayoutEvent 枚举. 页面布局模型构建和渲染期间引发的事件代码
type: docs
weight: 3370
url: /zh/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

页面布局模型构建和渲染期间引发的事件代码。

页面布局模型分两个步骤构建。 首先，“转换步骤”，这是页面布局提取文档内容并创建对象图的时候。 第二，“回流步骤”，这是结构被拆分、合并和排列的时候进入页面。

根据触发构建的操作，页面布局模型可能会也可能不会进一步呈现为固定页面格式。 例如，计算文档中的页面数或更新字段不需要呈现，而导出到 Pdf 则需要呈现。

```csharp
public enum PageLayoutEvent
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 默认值 |
| WatchDog | `1` | 对应于代码中经常访问且适合中止进程的检查点。 |
| BuildStarted | `2` | 页面布局的构建已开始。触发一次。 这是发生的第一个事件[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为. |
| BuildFinished | `3` | 页面布局的构建已完成。触发一次。 这是发生的最后一个事件[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为. |
| ConversionStarted | `4` | 文档模型到页面布局的转换已开始。触发一次。 当布局模型开始拉取文档内容时发生这种情况。 |
| ConversionFinished | `5` | 文档模型到页面布局的转换已完成。触发一次。 当布局模型停止拉动文档内容时会发生这种情况。 |
| ReflowStarted | `6` | 页面布局的重排已开始。触发一次。 当布局模型开始重排文档内容时会发生这种情况。 |
| ReflowFinished | `7` | 页面布局的回流已完成。触发一次。 当布局模型停止重排文档内容时会发生这种情况。 |
| PartReflowStarted | `8` | 页面回流已开始。 请注意，页面可能会回流多次，并且回流可能会在完成之前重新启动。 |
| PartReflowFinished | `9` | 页面的回流已完成。 请注意，页面可能会回流多次，并且回流可能会在完成之前重新启动。 |
| PartRenderingStarted | `10` | 页面渲染已开始。每页触发一次。 |
| PartRenderingFinished | `11` | 页面渲染已完成。每页触发一次。 |

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

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)


