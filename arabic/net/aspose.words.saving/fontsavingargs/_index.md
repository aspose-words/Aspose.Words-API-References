---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.FontSavingArgs فصل. يوفر بيانات لـFontSaving حدث في C#.
type: docs
weight: 5030
url: /ar/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

يوفر بيانات لـ[`FontSaving`](../ifontsavingcallback/fontsaving/) حدث.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class FontSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | يشير إلى ما إذا كان الخط الحالي غامقًا أم لا. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | الحصول على كائن المستند الذي يتم حفظه. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | يشير إلى اسم عائلة الخط الحالي. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | الحصول على أو تعيين اسم الملف (بدون مسار) حيث سيتم حفظ الخط. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | يسمح بتحديد التدفق الذي سيتم حفظ الخط فيه. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كمورد خط. الافتراضي هو`حقيقي` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | يسمح بتحديد ما إذا كان الخط الحالي سيتم تعيينه فرعيًا قبل التصدير كمورد خط. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | يشير إلى ما إذا كان الخط الحالي مائلًا أم لا. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الخط. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | يحصل على اسم ملف الخط الأصلي بامتداد. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | الحصول على حجم ملف الخط الأصلي. |

## ملاحظات

عندما يقوم Aspose.Words بحفظ مستند بتنسيق HTML أو التنسيقات ذات الصلة و[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) تم ضبط على`حقيقي`، فهو يحفظ كل موضوع خط لتصديره إلى ملف منفصل.

`FontSavingArgs` يتحكم في ما إذا كان يجب تصدير مورد خط معين وكيفية تصديره.

`FontSavingArgs`يسمح أيضًا بإعادة تعريف كيفية إنشاء أسماء ملفات الخطوط أو للتحايل تمامًا على حفظ الخطوط في الملفات عن طريق توفير كائنات الدفق الخاصة بك.

لتحديد ما إذا كنت تريد حفظ مورد خط معين، استخدم الأمر[`IsExportNeeded`](./isexportneeded/) ملكية.

لحفظ الخطوط في التدفقات بدلاً من الملفات، استخدم الملف[`FontStream`](./fontstream/) ملكية.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
