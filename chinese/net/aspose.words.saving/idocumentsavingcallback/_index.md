---
title: IDocumentSavingCallback Interface
linktitle: IDocumentSavingCallback
articleTitle: IDocumentSavingCallback
second_title: Aspose.Words for .NET
description: 实现 Aspose.Words.Saving.IDocumentSavingCallback 接口来创建文档的自定义保存方法，增强您的文档管理解决方案。
type: docs
weight: 5900
url: /zh/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

如果您希望在保存文档期间调用自己的自定义方法，请实现此接口。

```csharp
public interface IDocumentSavingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify/)(*[DocumentSavingArgs](../documentsavingargs/)*) | 这是为了通知文档保存进度。 |

## 例子

展示如何在保存为 html 的同时管理文档。

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // 支持以下格式：Html、Mhtml、Epub。
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// 保存进度回调。在“MaxDuration”秒后取消文档保存。
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// 中心。
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// 文档保存期间调用的回调方法。
    /// </summary>
    /// <param name="args">保存参数。</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// 开始保存文档的日期和时间。
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// 允许的最大持续时间（秒）。
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

展示如何在保存为 docx 的同时管理文档。

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // 支持以下格式：Docx、FlatOpc、Docm、Dotm、Dotx。
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// 保存进度回调。在“MaxDuration”秒后取消文档保存。
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// 中心。
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// 文档保存期间调用的回调方法。
    /// </summary>
    /// <param name="args">保存参数。</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// 开始保存文档的日期和时间。
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// 允许的最大持续时间（秒）。
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

展示如何在保存到 xamlflow 时管理文档。

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // 支持以下格式：XamlFlow、XamlFlowPack。
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// 保存进度回调。在“MaxDuration”秒后取消文档保存。
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// 中心。
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// 文档保存期间调用的回调方法。
    /// </summary>
    /// <param name="args">保存参数。</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// 开始保存文档的日期和时间。
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// 允许的最大持续时间（秒）。
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
