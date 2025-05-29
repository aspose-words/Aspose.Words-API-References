---
title: IDocumentLoadingCallback Interface
linktitle: IDocumentLoadingCallback
articleTitle: IDocumentLoadingCallback
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.IDocumentLoadingCallback 自定义文档加载。实现您自己的方法，以增强文档管理的控制力和灵活性。
type: docs
weight: 4080
url: /zh/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

如果您希望在加载文档期间调用自己的自定义方法，请实现此接口。

```csharp
public interface IDocumentLoadingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(*[DocumentLoadingArgs](../documentloadingargs/)*) | 这是为了通知文档加载进度。 |

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
