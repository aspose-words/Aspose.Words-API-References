---
title: DocumentSavingArgs Class
linktitle: DocumentSavingArgs
articleTitle: DocumentSavingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.DocumentSavingArgs، وهي ضرورية للتعامل مع أحداث حفظ المستندات بكفاءة في تطبيقاتك.
type: docs
weight: 5700
url: /ar/net/aspose.words.saving/documentsavingargs/
---
## DocumentSavingArgs class

تم تمرير وسيطة إلى[`Notify`](../idocumentsavingcallback/notify/) .

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public sealed class DocumentSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [EstimatedProgress](../../aspose.words.saving/documentsavingargs/estimatedprogress/) { get; } | النسبة المئوية الإجمالية المقدرة للتقدم. |

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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
