---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words لـ .NET
description: IDocumentLoadingCallback Notify طريقة. يتم استدعاؤه للإخطار بتقدم تحميل المستند في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

يتم استدعاؤه للإخطار بتقدم تحميل المستند.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| args | DocumentLoadingArgs | حجة الحدث. |

## ملاحظات

الاستخدامات الأساسية لهذه الواجهة هي السماح لرمز التطبيق بالحصول على حالة التقدم وإلغاء عملية التحميل.

يجب طرح استثناء من رد اتصال التقدم للإجهاض ويجب اكتشافه في كود المستهلك.

## أمثلة

يوضح كيفية إعلام المستخدم إذا تجاوز تحميل المستند وقت التحميل المتوقع.

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
/// قم بإلغاء تحميل مستند بعد ثواني "MaxDuration".
/// </summary>
public class LoadingProgressCallback : IDocumentLoadingCallback
{
    /// <summary>
    /// نسبة مئوية.
    /// </summary>
    public LoadingProgressCallback()
    {
        mLoadingStartedAt = DateTime.Now;
    }

    /// <summary>
    /// طريقة رد الاتصال التي يتم استدعاؤها أثناء تحميل المستند.
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
    /// التاريخ والوقت الذي يبدأ فيه تحميل المستند.
    /// </summary>
    private readonly DateTime mLoadingStartedAt;

    /// <summary>
    /// الحد الأقصى للمدة المسموح بها بالثواني.
    /// </summary>
    private const double MaxDuration = 0.5;
}
```

### أنظر أيضا

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
