---
title: IDocumentSavingCallback Interface
linktitle: IDocumentSavingCallback
articleTitle: IDocumentSavingCallback
second_title: Aspose.Words لـ .NET
description: قم بتنفيذ واجهة Aspose.Words.Saving.IDocumentSavingCallback لإنشاء طرق حفظ مخصصة للمستندات، مما يؤدي إلى تحسين حلول إدارة المستندات لديك.
type: docs
weight: 5900
url: /ar/net/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء حفظ مستند.

```csharp
public interface IDocumentSavingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.saving/idocumentsavingcallback/notify/)(*[DocumentSavingArgs](../documentsavingargs/)*) | يتم استدعاء هذا لإعلامك بتقدم حفظ المستند. |

## أمثلة

يوضح كيفية إدارة مستند أثناء الحفظ بتنسيق html.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // يتم دعم التنسيقات التالية: Html، Mhtml، Epub.
    HtmlSaveOptions saveOptions = new HtmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"HtmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// استدعاء متابعة الحفظ. إلغاء حفظ المستند بعد مرور "MaxDuration" ثانية.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// مركز.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة الاتصال الرجعي التي يتم استدعاؤها أثناء حفظ المستند.
    /// </summary>
    /// <param name="args">حفظ الوسائط.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// التاريخ والوقت الذي بدأت فيه عملية حفظ المستند.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.1d;
}
```

يوضح كيفية إدارة مستند أثناء الحفظ في docx.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // يتم دعم التنسيقات التالية: Docx، FlatOpc، Docm، Dotm، Dotx.
    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"OoxmlSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// استدعاء متابعة الحفظ. إلغاء حفظ المستند بعد مرور "MaxDuration" ثانية.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// مركز.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة الاتصال الرجعي التي يتم استدعاؤها أثناء حفظ المستند.
    /// </summary>
    /// <param name="args">حفظ الوسائط.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// التاريخ والوقت الذي بدأت فيه عملية حفظ المستند.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

يوضح كيفية إدارة مستند أثناء الحفظ في xamlflow.

```csharp
public void ProgressCallback(SaveFormat saveFormat, string ext)
{
    Document doc = new Document(MyDir + "Big document.docx");

    // يتم دعم التنسيقات التالية: XamlFlow، XamlFlowPack.
    XamlFlowSaveOptions saveOptions = new XamlFlowSaveOptions(saveFormat)
    {
        ProgressCallback = new SavingProgressCallback()
    };

    var exception = Assert.Throws<OperationCanceledException>(() =>
        doc.Save(ArtifactsDir + $"XamlFlowSaveOptions.ProgressCallback.{ext}", saveOptions));
    Assert.True(exception?.Message.Contains("EstimatedProgress"));
}

/// <summary>
/// استدعاء متابعة الحفظ. إلغاء حفظ المستند بعد مرور "MaxDuration" ثانية.
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// مركز.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة الاتصال الرجعي التي يتم استدعاؤها أثناء حفظ المستند.
    /// </summary>
    /// <param name="args">حفظ الوسائط.</param>
    public void Notify(DocumentSavingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mSavingStartedAt).TotalSeconds;
        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// التاريخ والوقت الذي بدأت فيه عملية حفظ المستند.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
