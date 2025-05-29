---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlSaveOptions ExportFontResources للتحكم في تصدير موارد الخطوط لتنسيقات HTML أو MHTML أو EPUB. حسّن مظهر مستندك!
type: docs
weight: 140
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

يحدد ما إذا كان يجب تصدير موارد الخط إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportFontResources { get; set; }
```

## ملاحظات

يسمح تصدير موارد الخطوط بتقديم مستند متسق بغض النظر عن الخطوط المتوفرة في بيئة المستخدم المحددة.

لو`ExportFontResources` تم ضبطه على`حقيقي` ، ستشير وثيقة HTML الرئيسية إلى كل خط عبر CSS 3**@الخط-الوجه** سيتم إخراج الخطوط والقواعد كملفات منفصلة. عند التصدير إلى تنسيقي IDPF EPUB أو MHTML ، سيتم تضمين الخطوط في الحزمة المقابلة مع الملفات الفرعية الأخرى.

لو[`ExportFontsAsBase64`](../exportfontsasbase64/) تم ضبطه على`حقيقي` لن يتم حفظ الخطوط في ملفات منفصلة. بدلاً من ذلك، سيتم تضمينها في**@الخط-الوجه** قواعد at في ترميز Base64.

**مهم!**عند تصدير موارد الخطوط، يجب مراعاة مسائل ترخيص الخطوط. يجب على المؤلفين الراغبين في استخدام خطوط محددة عبر آلية الخطوط القابلة للتنزيل التأكد بعناية من أن استخدامها المقصود يقع ضمن نطاق ترخيص الخطوط. لا تسمح العديد من الخطوط التجارية حاليًا بتنزيل خطوطها من الإنترنت بأي شكل من الأشكال. تنص اتفاقيات الترخيص التي تغطي بعض الخطوط تحديدًا على أن الاستخدام عبر**@الخط-الوجه** لا يُسمح باستخدام rules في أوراق أنماط CSS. قد يُخالف تقسيم الخطوط شروط الترخيص.

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

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
