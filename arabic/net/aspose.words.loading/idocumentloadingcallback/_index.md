---
title: Interface IDocumentLoadingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Loading.IDocumentLoadingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء تحميل مستند.
type: docs
weight: 3430
url: /ar/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء تحميل مستند.

```csharp
public interface IDocumentLoadingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(DocumentLoadingArgs) | يتم استدعاء هذا لإخطار تقدم تحميل المستند. |

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)


