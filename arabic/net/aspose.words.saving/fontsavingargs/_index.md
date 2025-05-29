---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.FontSavingArgs—تعزيز معالجة المستندات باستخدام بيانات حدث FontSaving التفصيلية لتحقيق التخصيص والتحكم الفائقين.
type: docs
weight: 5780
url: /ar/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

يوفر بيانات لـ[`FontSaving`](../ifontsavingcallback/fontsaving/) الحدث.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class FontSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | يشير إلى ما إذا كان الخط الحالي غامقًا. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | يحصل على كائن المستند الذي يتم حفظه. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | يشير إلى اسم عائلة الخط الحالية. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | يحصل على اسم الملف (بدون مسار) الذي سيتم حفظ الخط فيه أو يعينه. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ الخط فيه. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كمورد خط. الإعداد الافتراضي هو`حقيقي` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | يسمح بتحديد ما إذا كان سيتم تقسيم الخط الحالي قبل تصديره كمورد خط. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | يشير إلى ما إذا كان الخط الحالي مائلًا. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الخط. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | يحصل على اسم ملف الخط الأصلي مع الامتداد. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | يحصل على حجم ملف الخط الأصلي. |

## ملاحظات

عندما يقوم Aspose.Words بحفظ مستند بتنسيق HTML أو تنسيقات ذات صلة و[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) تم تعيين على`حقيقي`، فهو يحفظ كل موضوع خط للتصدير في ملف منفصل.

`FontSavingArgs` يتحكم فيما إذا كان ينبغي تصدير مورد خط معين وكيفية القيام بذلك.

`FontSavingArgs`يسمح أيضًا بإعادة تعريف كيفية إنشاء أسماء ملفات الخطوط أو التحايل تمامًا على حفظ الخطوط في الملفات من خلال توفير كائنات التدفق الخاصة بك.

لتحديد ما إذا كنت تريد حفظ مورد خط معين، استخدم[`IsExportNeeded`](./isexportneeded/) ملكية.

لحفظ الخطوط في التدفقات بدلاً من الملفات، استخدم[`FontStream`](./fontstream/) ملكية.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
