---
title: PageSavingArgs.PageStream
linktitle: PageStream
articleTitle: PageStream
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageStream في PageSavingArgs، التي تتيح لك حفظ صفحة المستند بسلاسة في التدفق المطلوب لإدارة الملفات بكفاءة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

يسمح بتحديد الدفق الذي سيتم حفظ صفحة المستند فيه.

```csharp
public Stream PageStream { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية حفظ صفحات المستندات في التدفقات بدلاً من الملفات.

القيمة الافتراضية هي`باطل` . عندما تكون هذه الخاصية`باطل` سيتم حفظ صفحة المستند في الملف المحدد في[`PageFileName`](../pagefilename/) ملكية.

إذا كان كلاهما`PageStream` و[`PageFileName`](../pagefilename/) إذا تم تعيينها، فسيتم استخدام PageStream.

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

* class [PageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
