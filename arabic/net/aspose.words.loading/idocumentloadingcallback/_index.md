---
title: Interface IDocumentLoadingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Loading.IDocumentLoadingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي يتم استدعاؤها أثناء تحميل المستند.
type: docs
weight: 3630
url: /ar/net/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد أن يكون لديك طريقتك المخصصة التي يتم استدعاؤها أثناء تحميل المستند.

```csharp
public interface IDocumentLoadingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Notify](../../aspose.words.loading/idocumentloadingcallback/notify/)(DocumentLoadingArgs) | يتم استدعاؤه للإخطار بتقدم تحميل المستند. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)


