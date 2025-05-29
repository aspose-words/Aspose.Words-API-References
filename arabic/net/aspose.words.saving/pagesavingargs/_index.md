---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.PageSavingArgs، وهي أساسية لتحسين معالجة المستندات باستخدام بيانات أحداث PageSaving المفصلة. حسّن سير عملك!
type: docs
weight: 6160
url: /ar/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

يوفر بيانات لـ[`PageSaving`](../ipagesavingcallback/pagesaving/) الحدث.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public class PageSavingArgs
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ صفحة المستند. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | يحصل على اسم الملف الذي سيتم حفظ صفحة المستند فيه أو يعينه. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | فهرس الصفحة الحالية. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ صفحة المستند فيه. |

## أمثلة

يوضح كيفية استخدام معاودة الاتصال لحفظ مستند في صفحة HTML تلو الأخرى.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // سوف نقوم بحفظ كل صفحة في هذا المستند في ملف HTML منفصل في نظام الملفات المحلي.
    // قم بتعيين معاودة اتصال تسمح لنا بتسمية كل مستند HTML الناتج.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// يحفظ جميع الصفحات في الملف والدليل المحددين بداخله.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل صفحة من المستند.
        // 1 - تعيين اسم ملف لملف الصفحة الناتج:
        args.PageFileName = outFileName;

        // 2 - إنشاء تدفق مخصص لملف الصفحة الناتج:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
