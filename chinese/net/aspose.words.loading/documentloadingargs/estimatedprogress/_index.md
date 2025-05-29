---
title: DocumentLoadingArgs.EstimatedProgress
linktitle: EstimatedProgress
articleTitle: EstimatedProgress
second_title: Aspose.Words for .NET
description: 使用 DocumentLoadingArgs 的 EstimatedProgress 属性轻松跟踪进度，提供实时百分比更新以提高效率。
type: docs
weight: 10
url: /zh/net/aspose.words.loading/documentloadingargs/estimatedprogress/
---
## DocumentLoadingArgs.EstimatedProgress property

总体预计进度百分比。

```csharp
public double EstimatedProgress { get; }
```

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

* class [DocumentLoadingArgs](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
