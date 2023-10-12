---
title: Class PageSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PageSavingArgs فصل. يوفر بيانات لـPageSaving حدث.
type: docs
weight: 5380
url: /ar/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

يوفر بيانات لـ[`PageSaving`](../ipagesavingcallback/pagesaving/) حدث.

لمعرفة المزيد، قم بزيارة[البرمجة بالوثائق](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

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
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | الحصول على أو تعيين اسم الملف الذي سيتم حفظ صفحة المستند فيه. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | فهرس الصفحة الحالية. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | يسمح بتحديد التدفق الذي سيتم حفظ صفحة المستند فيه. |

### أمثلة

يوضح كيفية استخدام رد الاتصال لحفظ مستند إلى HTML صفحة تلو الأخرى.

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

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // سنقوم بحفظ كل صفحة في هذا المستند في ملف HTML منفصل في نظام الملفات المحلي.
    // قم بتعيين رد اتصال يسمح لنا بتسمية كل مستند HTML مخرج.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// يحفظ جميع الصفحات في ملف ودليل محددين فيه.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل صفحة من المستند.
        // 1 - قم بتعيين اسم ملف لملف صفحة الإخراج:
        args.PageFileName = outFileName;

        // 2 - إنشاء دفق مخصص لملف صفحة الإخراج:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


