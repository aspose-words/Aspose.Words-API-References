---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ExportFontResources ملكية. يحدد ما إذا كان يجب تصدير موارد الخطوط إلى HTML أو MHTML أو EPUB. الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

يحدد ما إذا كان يجب تصدير موارد الخطوط إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportFontResources { get; set; }
```

## ملاحظات

يتيح تصدير موارد الخطوط عرضًا متسقًا للمستندات بشكل مستقل عن الخطوط المتاحة في بيئة مستخدم معين.

لو`ExportFontResources` تم ضبطه على`حقيقي` ، سيشير مستند HTML الرئيسي إلى كل خط عبر CSS 3**@الخط الوجه** سيتم إخراج القاعدة والخطوط كملفات منفصلة. عند التصدير إلى تنسيقات IDPF EPUB أو MHTML ، سيتم تضمين الخطوط في الحزمة المقابلة مع الملفات الفرعية الأخرى.

لو[`ExportFontsAsBase64`](../exportfontsasbase64/) تم ضبطه على`حقيقي`، لن يتم حفظ الخطوط في ملفات منفصلة. بدلاً من ذلك، سيتم تضمينها في**@الخط الوجه** القواعد في ترميز Base64.

**مهم!** عند تصدير موارد الخطوط، يجب مراعاة مشكلات ترخيص الخطوط. يجب على المؤلفين الذين يرغبون في استخدام خطوط معينة عبر آلية الخط القابلة للتنزيل أن يتحققوا دائمًا بعناية من أن الاستخدام المقصود يقع ضمن نطاق ترخيص الخط. لا تسمح العديد من الخطوط التجارية في الوقت الحالي بتنزيل خطوطها من الويب بأي شكل من الأشكال. تشير اتفاقيات الترخيص التي تغطي بعض الخطوط على وجه التحديد إلى أن الاستخدام عبر**@الخط الوجه** Rules غير مسموح به في أوراق أنماط CSS. يمكن أن يؤدي تعيين الخط الفرعي أيضًا إلى انتهاك شروط الترخيص.

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

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
