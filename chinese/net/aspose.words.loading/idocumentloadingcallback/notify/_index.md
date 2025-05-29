---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words for .NET
description: 使用 IDocumentLoadingCallback 的 Notify 方法轻松追踪文档加载进度。实时更新，提升用户体验！
type: docs
weight: 10
url: /zh/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

这是为了通知文档加载进度。

```csharp
public void Notify(DocumentLoadingArgs args)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | DocumentLoadingArgs | 事件的一个论点。 |

## 评论

此接口的主要用途是允许应用程序代码获取进度状态并中止加载过程。

应该从中止的进度回调中抛出一个异常，并且应该在消费者代码中捕获它。

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
