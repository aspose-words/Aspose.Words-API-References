---
title: Notify
second_title: Aspose.Words for .NET API 参考
description: 调用此函数以通知文档保存进度
type: docs
weight: 10
url: /zh/net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

调用此函数以通知文档保存进度。

```csharp
public void Notify(DocumentSavingArgs args)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | DocumentSavingArgs | 事件的论据。 |

### 评论

此接口的主要用途是允许应用程序代码获取进度状态并中止保存过程。

应该从进度回调中抛出异常以进行中止，并且应该在消费者代码中捕获该异常。

### 例子

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
    /// 文档保存时调用的回调方法。
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
    /// 允许的最大持续时间（以秒为单位）。
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

展示如何在保存到 docx 的同时管理文档。

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
    /// 文档保存时调用的回调方法。
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
    /// 允许的最大持续时间（以秒为单位）。
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

演示如何在保存到 xamlflow 时管理文档。

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
    /// 文档保存时调用的回调方法。
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
    /// 允许的最大持续时间（以秒为单位）。
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### 也可以看看

* class [DocumentSavingArgs](../../documentsavingargs)
* interface [IDocumentSavingCallback](../../idocumentsavingcallback)
* 命名空间 [Aspose.Words.Saving](../../idocumentsavingcallback)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
