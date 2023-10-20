---
title: IDocumentSavingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words لـ .NET
description: IDocumentSavingCallback Notify طريقة. يتم استدعاؤه للإخطار بتقدم عملية حفظ المستند في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback.Notify method

يتم استدعاؤه للإخطار بتقدم عملية حفظ المستند.

```csharp
public void Notify(DocumentSavingArgs args)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| args | DocumentSavingArgs | حجة الحدث. |

## ملاحظات

الاستخدامات الأساسية لهذه الواجهة هي السماح لرمز التطبيق بالحصول على حالة التقدم وإلغاء عملية الحفظ.

يجب طرح استثناء من رد اتصال التقدم للإجهاض ويجب اكتشافه في كود المستهلك.

## أمثلة

يوضح كيفية إدارة مستند أثناء حفظه في html.

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
/// رد اتصال حفظ التقدم. قم بإلغاء حفظ مستند بعد ثواني "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// نسبة مئوية.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة رد الاتصال التي يتم استدعاؤها أثناء حفظ المستند.
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
    /// التاريخ والوقت الذي يبدأ فيه حفظ المستندات.
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
/// رد اتصال حفظ التقدم. قم بإلغاء حفظ مستند بعد ثواني "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// نسبة مئوية.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة رد الاتصال التي يتم استدعاؤها أثناء حفظ المستند.
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
    /// التاريخ والوقت الذي يبدأ فيه حفظ المستندات.
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
/// رد اتصال حفظ التقدم. قم بإلغاء حفظ مستند بعد ثواني "MaxDuration".
/// </summary>
public class SavingProgressCallback : IDocumentSavingCallback
{
    /// <summary>
    /// نسبة مئوية.
    /// </summary>
    public SavingProgressCallback()
    {
        mSavingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة رد الاتصال التي يتم استدعاؤها أثناء حفظ المستند.
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
    /// التاريخ والوقت الذي يبدأ فيه حفظ المستندات.
    /// </summary>
    private readonly DateTime mSavingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.01d;
}
```

### أنظر أيضا

* class [DocumentSavingArgs](../../documentsavingargs/)
* interface [IDocumentSavingCallback](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
