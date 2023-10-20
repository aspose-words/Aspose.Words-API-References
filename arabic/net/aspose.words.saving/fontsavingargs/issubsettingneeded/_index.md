---
title: FontSavingArgs.IsSubsettingNeeded
linktitle: IsSubsettingNeeded
articleTitle: IsSubsettingNeeded
second_title: Aspose.Words لـ .NET
description: FontSavingArgs IsSubsettingNeeded ملكية. يسمح بتحديد ما إذا كان الخط الحالي سيتم تعيينه فرعيًا قبل التصدير كمورد خط في C#.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

يسمح بتحديد ما إذا كان الخط الحالي سيتم تعيينه فرعيًا قبل التصدير كمورد خط.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

## ملاحظات

يمكن تصدير الخطوط كملفات خطوط أصلية كاملة أو تجميعها فرعيًا لتضمين الأحرف المستخدمة في المستند فقط. يسمح الإعداد الفرعي بتقليل حجم مورد الخط الناتج.

افتراضيًا، يقرر Aspose.Words ما إذا كان سيتم إجراء الإعداد الفرعي أم لا من خلال مقارنة حجم ملف الخط الأصلي مع الحجم المحدد في[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . يمكنك تجاوز هذا السلوك للخطوط الفردية عن طريق تعيين`IsSubsettingNeeded` ملكية.

## أمثلة

يوضح كيفية تحديد المنطق المخصص لتصدير الخطوط عند الحفظ إلى HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // تكوين كائن SaveOptions لتصدير الخطوط إلى ملفات منفصلة.
    // قم بتعيين رد اتصال يتعامل مع حفظ الخط بطريقة مخصصة.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // سيقوم رد الاتصال بتصدير ملفات .ttf وحفظها بجانب المستند الناتج.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// يطبع معلومات حول الخطوط المصدرة ويحفظها في نفس مجلد النظام المحلي مثل مخرجاتها .html.
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

        // هناك طريقتان لحفظ الخط المُصدَّر.
        // 1 - احفظه في موقع نظام الملفات المحلي:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - احفظه في الدفق:
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
