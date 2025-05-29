---
title: SaveOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: Aspose.Words for .NET
description: 使用 SaveOptions ProgressCallback 属性增强您的文档保存体验，为无缝工作流程提供保存进度的实时更新。
type: docs
weight: 120
url: /zh/net/aspose.words.saving/saveoptions/progresscallback/
---
## SaveOptions.ProgressCallback property

在保存文档期间调用并接受有关保存进度的数据。

```csharp
public IDocumentSavingCallback ProgressCallback { get; set; }
```

## 评论

保存到时报告进度Docx，FlatOpc , Docm，Dotm，Dotx , Doc，Dot , Html，Mhtml，Epub , XamlFlow， 或者XamlFlowPack.

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

* interface [IDocumentSavingCallback](../../idocumentsavingcallback/)
* class [SaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
