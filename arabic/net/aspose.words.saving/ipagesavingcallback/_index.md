---
title: IPageSavingCallback Interface
linktitle: IPageSavingCallback
articleTitle: IPageSavingCallback
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.IPageSavingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ صفحات منفصلة عند حفظ مستند بتنسيقات صفحات ثابتة في C#.
type: docs
weight: 5180
url: /ar/net/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ صفحات منفصلة عند حفظ مستند بتنسيقات صفحات ثابتة.

```csharp
public interface IPageSavingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [PageSaving](../../aspose.words.saving/ipagesavingcallback/pagesaving/)(*[PageSavingArgs](../pagesavingargs/)*) | يتم استدعاؤه عندما يقوم Aspose.Words بحفظ صفحة منفصلة في تنسيقات الصفحات الثابتة. |

## أمثلة

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
