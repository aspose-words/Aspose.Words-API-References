---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.PageLayoutEvent 枚举——在文档渲染和构建过程中优化页面布局事件的关键。立即增强您的工作流程！
type: docs
weight: 3820
url: /zh/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

页面布局模型构建和渲染期间引发的事件代码。

页面布局模型分两个步骤构建。 首先是“转换步骤”，这是页面布局提取文档内容并创建对象图的步骤。 其次是“回流步骤”，这是将结构拆分、合并并排列成页面的步骤。

根据触发构建的操作，页面布局模型可能会或可能不会进一步呈现为固定页面格式。 例如，计算文档中的页数或更新字段不需要渲染，而导出为 PDF 则需要。

```csharp
public enum PageLayoutEvent
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 默认值 |
| WatchDog | `1` | 对应于代码中经常访问且适合中止进程的检查点。 |
| BuildStarted | `2` | 页面布局构建已开始。触发一次。 这是第一个事件，当[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为。 |
| BuildFinished | `3` | 页面布局构建已完成。触发一次。 这是最后一个事件，发生在[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)被称为。 |
| ConversionStarted | `4` | 文档模型已开始转换为页面布局。触发一次。 当布局模型开始提取文档内容时触发。 |
| ConversionFinished | `5` | 文档模型到页面布局的转换已完成。触发一次。 当布局模型停止提取文档内容时，触发此操作。 |
| ReflowStarted | `6` | 页面布局重排已开始。触发一次。 当布局模型开始重排文档内容时，会发生此事件。 |
| ReflowFinished | `7` | 页面布局重排已完成。触发一次。 当布局模型停止重排文档内容时，会发生此事件。 |
| PartReflowStarted | `8` | 页面重排已开始。 请注意，页面可能会重排多次，并且重排可能会在完成之前重新启动。 |
| PartReflowFinished | `9` | 页面重排已完成。 请注意，页面可能会重排多次，并且重排可能会在完成之前重新启动。 |
| PartRenderingStarted | `10` | 页面渲染已开始。每个页面触发一次。 |
| PartRenderingFinished | `11` | 页面渲染已完成。此事件每页触发一次。 |

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
