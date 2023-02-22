---
title: PageSavingArgs.PageStream
second_title: Aspose.Words لمراجع .NET API
description: PageSavingArgs ملكية. يسمح بتحديد التدفق حيث سيتم حفظ صفحة المستند فيه.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pagesavingargs/pagestream/
---
## PageSavingArgs.PageStream property

يسمح بتحديد التدفق حيث سيتم حفظ صفحة المستند فيه.

```csharp
public Stream PageStream { get; set; }
```

### ملاحظات

تتيح لك هذه الخاصية حفظ صفحات المستند في التدفقات بدلاً من الملفات.

النظام الأساسي`لا شيء` . عندما تكون هذه الخاصية`لا شيء`، سيتم حفظ صفحة المستند في ملف محدد في[`PageFileName`](../pagefilename/) منشأه.

إذا تم تعيين كل من PageStream و PageFileName ، فسيتم استخدام PageStream.

### أمثلة

يوضح كيفية استخدام رد نداء لحفظ مستند إلى صفحة HTML بصفحة.

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

    // قم بإنشاء كائن "HtmlFixedSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // سنحفظ كل صفحة في هذا المستند في ملف HTML منفصل في نظام الملفات المحلي.
    // تعيين رد اتصال يسمح لنا بتسمية كل مستند HTML ناتج.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// يحفظ كل الصفحات في ملف ودليل محدد بداخله.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // فيما يلي طريقتان لتحديد مكان حفظ Aspose.Words كل صفحة من المستند.
        // 1 - حدد اسم ملف لملف صفحة الإخراج:
        args.PageFileName = outFileName;

        // 2 - إنشاء دفق مخصص لملف صفحة الإخراج:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### أنظر أيضا

* class [PageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../pagesavingargs/)
* المجسم [Aspose.Words](../../../)


