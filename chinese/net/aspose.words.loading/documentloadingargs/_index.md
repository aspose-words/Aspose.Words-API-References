---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Loading.DocumentLoadingArgs 类，实现高效的文档加载。使用强大的通知参数增强您的工作流程。
type: docs
weight: 4040
url: /zh/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

传入的参数[`Notify`](../idocumentloadingcallback/notify/).

要了解更多信息，请访问[指定加载选项](https://docs.aspose.com/words/net/specify-load-options/)文档文章。

```csharp
public sealed class DocumentLoadingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | 总体预计进度百分比。 |

## 例子

显示文档加载时间超出预期时如何通知用户。

```csharp
public void ProgressCallback()
{
    LoadingProgressCallback progressCallback = new LoadingProgressCallback();

    LoadOptions loadOptions = new LoadOptions { ProgressCallback = progressCallback };

    try
    {
        Document doc = new Document(MyDir + "Big document.docx", loadOptions);
    }
    catch (OperationCanceledException exception)
    {
        Console.WriteLine(exception.Message);

        // 处理加载持续时间问题。
    }
}

/// <summary>
/// 在“MaxDuration”秒后取消文档加载。
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// 中心。
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// 在文档加载期间调用的回调方法。
    /// </summary>
    /// <param name="args">正在加载参数。</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// 开始文档加载的日期和时间。
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// 允许的最大持续时间（秒）。
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
