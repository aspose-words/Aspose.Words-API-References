---
title: FontSavingArgs.KeepFontStreamOpen
linktitle: KeepFontStreamOpen
articleTitle: KeepFontStreamOpen
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تسمح خاصية KeepFontStreamOpen في FontSavingArgs لبرنامج Aspose.Words بإدارة تدفقات الخطوط بكفاءة، مما يعزز تجربة معالجة المستندات لديك.
type: docs
weight: 90
url: /ar/net/aspose.words.saving/fontsavingargs/keepfontstreamopen/
---
## FontSavingArgs.KeepFontStreamOpen property

يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الخط.

```csharp
public bool KeepFontStreamOpen { get; set; }
```

## ملاحظات

الافتراضي هو`خطأ شنيع` وسوف يقوم Aspose.Words بإغلاق الدفق الذي قدمته في[`FontStream`](../fontstream/) الخاصية بعد كتابة الخط فيها. حدد`حقيقي` للحفاظ على مجرى النهر مفتوحا.

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
