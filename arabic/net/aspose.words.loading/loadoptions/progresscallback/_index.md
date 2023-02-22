---
title: LoadOptions.ProgressCallback
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. يتم الاتصال به أثناء تحميل مستند ويقبل البيانات حول تقدم التحميل.
type: docs
weight: 130
url: /ar/net/aspose.words.loading/loadoptions/progresscallback/
---
## LoadOptions.ProgressCallback property

يتم الاتصال به أثناء تحميل مستند ويقبل البيانات حول تقدم التحميل.

```csharp
public IDocumentLoadingCallback ProgressCallback { get; set; }
```

### ملاحظات

Docx وFlatOpc وDocm وDotm وDotx وMarkdown وRtf وWordML وDoc وDot وOdt وOtt الصيغ المدعومة.

### أمثلة

يوضح كيفية إعلام المستخدم إذا تجاوز تحميل المستند وقت التحميل المتوقع.

```csharp
[Test]
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

        // معالجة مشكلة مدة التحميل.
    }
}

/// <summary>
/// إلغاء تحميل مستند بعد ثوان "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// تحكم.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة رد الاتصال التي تم استدعاؤها أثناء تحميل المستند.
    /// </summary>
    /// < param name = "args" > تحميل الوسائط. < / param >
    public void Notify(DocumentLoadingArgs args)
    {
        DateTime canceledAt = DateTime.Now;
        double ellapsedSeconds = (canceledAt - mLoadingStartedAt).TotalSeconds;

        if (ellapsedSeconds > MaxDuration)
            throw new OperationCanceledException($"EstimatedProgress = {args.EstimatedProgress}; CanceledAt = {canceledAt}");
    }

    /// <summary>
    /// تاريخ ووقت بدء تحميل المستند.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// أقصى مدة مسموح بها بالثانية.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### أنظر أيضا

* interface [IDocumentLoadingCallback](../../idocumentloadingcallback/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


