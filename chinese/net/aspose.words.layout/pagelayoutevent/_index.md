---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Layout.PageLayoutEvent 枚举. 在页面布局模型构建和渲染期间引发的事件代码 在 C#.
type: docs
weight: 3370
url: /zh/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

在页面布局模型构建和渲染期间引发的事件代码。

页面布局模型的建立分为两个步骤。 第一，“转换步骤”，这是页面布局拉文档内容并创建对象图的时候。 第二，“回流步骤”，这是对结构进行拆分，合并和排列的时候成页面。

根据触发构建的操作，页面布局模型可能会或可能不会进一步呈现为固定的页面格式。 例如，计算文档中的页数或更新字段不需要呈现，而导出为 Pdf 则需要。

```csharp
public enum PageLayoutEvent
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 默认值 |
| WatchDog | `1` | 对应于代码中经常被访问且适合中止进程的检查点。 |
| BuildStarted | `2` | 页面布局的构建已经开始。触发一次。 这是第一个发生的事件[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为. |
| BuildFinished | `3` | 页面布局的构建已经完成。触发一次。 这是最后一次发生的事件[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为. |
| ConversionStarted | `4` | 文档模型到页面布局的转换已经开始。触发一次。 当布局模型开始提取文档内容时发生。 |
| ConversionFinished | `5` | 文档模型到页面布局的转换已完成。触发一次。 当布局模型停止拉取文档内容时发生。 |
| ReflowStarted | `6` | 页面布局的回流已经开始。触发一次。 当布局模型开始重排文档内容时发生。 |
| ReflowFinished | `7` | 页面布局的重排已完成。触发一次。 当布局模型停止重排文档内容时发生。 |
| PartReflowStarted | `8` | 页面的回流已经开始。 请注意，页面可能会多次回流，回流可能会在完成之前重新开始。 |
| PartReflowFinished | `9` | 页面回流已完成。 请注意，页面可能会多次回流，并且回流可能在完成之前重新开始。 |
| PartRenderingStarted | `10` | 页面渲染已开始。每页触发一次。 |
| PartRenderingFinished | `11` | 页面渲染已完成。每页触发一次。 |

## 例子

展示如何使用布局回调跟踪布局更改。

```csharp
[Test]
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
/// 并渲染一个页面，我们在本地文件系统中的图像上执行页面回流。
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
