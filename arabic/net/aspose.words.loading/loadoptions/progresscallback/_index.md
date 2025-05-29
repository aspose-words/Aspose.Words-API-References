---
title: LoadOptions.ProgressCallback
linktitle: ProgressCallback
articleTitle: ProgressCallback
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LoadOptions ProgressCallback لتتبع تقدم تحميل المستندات بكفاءة. حسّن أداء تطبيقك وتجربة المستخدم!
type: docs
weight: 130
url: /ar/net/aspose.words.loading/loadoptions/progresscallback/
---
## LoadOptions.ProgressCallback property

يتم استدعاؤها أثناء تحميل مستند وتقبل البيانات حول تقدم التحميل.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

## ملاحظات

Docx ،FlatOpc ،Docm ،Dotm ،Dotx ،Markdown ،Rtf ،WordML ،Doc ،Dot ،Odt ،Ott التنسيقات المدعومة.

## أمثلة

يوضح كيفية إخطار المستخدم إذا تجاوز تحميل المستند وقت التحميل المتوقع.

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

        // التعامل مع مشكلة مدة التحميل.
    }
}

/// <summary>
/// إلغاء تحميل المستند بعد مرور "MaxDuration" ثانية.
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// مركز.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة الاتصال الرجعي التي يتم استدعاؤها أثناء تحميل المستند.
    /// </summary>
    /// <param name="args">جاري تحميل الوسائط.</param>
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// التاريخ والوقت الذي بدأ فيه تحميل المستند.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### أنظر أيضا

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
