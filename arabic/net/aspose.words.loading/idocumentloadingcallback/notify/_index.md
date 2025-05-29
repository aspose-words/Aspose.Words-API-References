---
title: IDocumentLoadingCallback.Notify
linktitle: Notify
articleTitle: Notify
second_title: Aspose.Words لـ .NET
description: تتبع عملية تحميل المستندات بسهولة باستخدام طريقة IDocumentLoadingCallback Notify. حسّن تجربة المستخدم بتحديثات آنية!
type: docs
weight: 10
url: /ar/net/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback.Notify method

يتم استدعاء هذا لإعلامك بتقدم تحميل المستند.

```csharp
public void Notify(DocumentLoadingArgs args)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| args | DocumentLoadingArgs | حجة الحدث. |

## ملاحظات

الاستخدامات الأساسية لهذه الواجهة هي السماح لكود التطبيق بالحصول على حالة التقدم وإلغاء عملية التحميل.

يجب أن يتم طرح استثناء من استدعاء التقدم للإجهاض ويجب التقاطه في كود المستهلك.

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

* property [ProgressCallback](../../loadoptions/progresscallback/)
* class [DocumentLoadingArgs](../../documentloadingargs/)
* interface [IDocumentLoadingCallback](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
