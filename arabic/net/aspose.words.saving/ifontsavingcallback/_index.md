---
title: Interface IFontSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.IFontSavingCallback واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي إشعارات والتحكم في how يحفظ Aspose.Words الخطوط عند تصدير مستند إلى تنسيق HTML .
type: docs
weight: 4900
url: /ar/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد تلقي إشعارات والتحكم في how يحفظ Aspose.Words الخطوط عند تصدير مستند إلى تنسيق HTML .

```csharp
public interface IFontSavingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(FontSavingArgs) | يتم الاتصال به عندما يكون Aspose.Words على وشك حفظ مورد الخط. |

### أمثلة

يوضح كيفية تحديد منطق مخصص لتصدير الخطوط عند الحفظ بتنسيق HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // تكوين كائن SaveOptions لتصدير الخطوط إلى ملفات منفصلة.
    // تعيين رد اتصال يعالج حفظ الخط بطريقة مخصصة.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // ستصدر رد النداء ملفات .ttf وحفظها بجانب المستند الناتج.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

/// <summary>
/// يطبع معلومات حول الخطوط المصدرة ويحفظها في نفس مجلد النظام المحلي مثل إخراجها .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // يمكننا أيضًا الوصول إلى المستند المصدر من هنا.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // هناك طريقتان لحفظ الخط الذي تم تصديره.
        // 1 - احفظه في موقع نظام ملفات محلي:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - احفظه في دفق:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


