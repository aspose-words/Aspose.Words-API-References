---
title: DocumentLoadingArgs Class
linktitle: DocumentLoadingArgs
articleTitle: DocumentLoadingArgs
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Loading.DocumentLoadingArgs لتحميل المستندات بكفاءة. حسّن سير عملك باستخدام وسيطات إشعارات فعّالة.
type: docs
weight: 4040
url: /ar/net/aspose.words.loading/documentloadingargs/
---
## DocumentLoadingArgs class

تم تمرير وسيطة إلى[`Notify`](../idocumentloadingcallback/notify/) .

لمعرفة المزيد، قم بزيارة[تحديد خيارات التحميل](https://docs.aspose.com/words/net/specify-load-options/) مقالة توثيقية.

```csharp
public sealed class DocumentLoadingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EstimatedProgress](../../aspose.words.loading/documentloadingargs/estimatedprogress/) { get; } | النسبة المئوية الإجمالية المقدرة للتقدم. |

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
