---
title: FontSavingArgs.IsExportNeeded
linktitle: IsExportNeeded
articleTitle: IsExportNeeded
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontSavingArgs IsExportNeeded للتحكم في تصدير موارد الخطوط. حسّن كفاءة مشروعك بإعدادات قابلة للتخصيص!
type: docs
weight: 60
url: /ar/net/aspose.words.saving/fontsavingargs/isexportneeded/
---
## FontSavingArgs.IsExportNeeded property

يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كمورد خط. الإعداد الافتراضي هو`حقيقي` .

```csharp
public bool IsExportNeeded { get; set; }
```

## أمثلة

يوضح كيفية تحديد منطق مخصص لتصدير الخطوط عند الحفظ في HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // قم بتكوين كائن SaveOptions لتصدير الخطوط إلى ملفات منفصلة.
    // قم بتعيين معاودة الاتصال التي ستتعامل مع حفظ الخط بطريقة مخصصة.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // ستقوم وظيفة معاودة الاتصال بتصدير ملفات .ttf وحفظها إلى جانب مستند الإخراج.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// يطبع معلومات حول الخطوط المصدرة ويحفظها في نفس مجلد النظام المحلي مثل ملف .html الناتج عنها.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        //يمكننا أيضًا الوصول إلى المستند المصدر من هنا.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // هناك طريقتان لحفظ الخط المُصدَّر.
        // 1 - احفظه في موقع نظام الملفات المحلي:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - احفظه في مجرى:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### أنظر أيضا

* class [FontSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
