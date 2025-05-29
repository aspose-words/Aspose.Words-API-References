---
title: IPageSavingCallback.PageSaving
linktitle: PageSaving
articleTitle: PageSaving
second_title: Aspose.Words لـ .NET
description: اكتشف وظيفة iPageSavingCallback في Aspose.Words، المصممة لتحسين حفظ الصفحات بتنسيقات ثابتة. حسّن إدارة مستنداتك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.saving/ipagesavingcallback/pagesaving/
---
## IPageSavingCallback.PageSaving method

يتم استدعاؤها عندما يحفظ Aspose.Words صفحة منفصلة بتنسيقات صفحات ثابتة.

```csharp
public void PageSaving(PageSavingArgs args)
```

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

* class [PageSavingArgs](../../pagesavingargs/)
* interface [IPageSavingCallback](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
