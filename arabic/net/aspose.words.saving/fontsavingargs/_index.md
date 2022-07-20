---
title: FontSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: توفير بيانات لملفFontSaving./ifontsavingcallback/fontsaving الحدث ._ x000d_
type: docs
weight: 4770
url: /ar/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

توفير بيانات لملف[`FontSaving`](../ifontsavingcallback/fontsaving) الحدث ._ x000d_

```csharp
public class FontSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold) { get; } | يشير إلى ما إذا كان الخط الحالي غامقًا . |
| [Document](../../aspose.words.saving/fontsavingargs/document) { get; } | يحصل على كائن المستند الذي يتم حفظه . |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname) { get; } | يشير إلى اسم عائلة الخط الحالي. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename) { get; set; } | الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ الخط فيه. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream) { get; set; } | يسمح بتحديد التدفق حيث سيتم حفظ الخط فيه. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded) { get; set; } | يسمح بتحديد ما إذا كان سيتم تصدير الخط الحالي كمورد خطوط. الافتراضي هو`حقيقي` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded) { get; set; } | يسمح بتحديد ما إذا كان سيتم تقسيم الخط الحالي قبل التصدير كمورد للخط. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic) { get; } | يشير إلى ما إذا كان الخط الحالي مائلاً. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الخط. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename) { get; } | يحصل على اسم ملف الخط الأصلي بامتداد . |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize) { get; } | يحصل على حجم ملف الخط الأصلي. |

### ملاحظات

عندما يحفظ Aspose.Words مستندًا بتنسيق HTML أو تنسيقات ذات صلة وملفات[`ExportFontResources`](../htmlsaveoptions/exportfontresources) تم ضبط على **حقيقي**، فإنه يحفظ كل موضوع خط للتصدير إلى ملف منفصل.

[`FontSavingArgs`](../fontsavingargs) يتحكم في ما إذا كان يجب تصدير مورد خط معين وكيفية ذلك.

[`FontSavingArgs`](../fontsavingargs)يسمح أيضًا بإعادة تعريف كيفية إنشاء أسماء ملفات الخطوط أو التحايل تمامًا على حفظ الخطوط في الملفات من خلال توفير كائنات البث الخاصة بك.

لتحديد ما إذا كنت تريد حفظ مورد خط معين ، استخدم امتداد[`IsExportNeeded`](./isexportneeded) منشأه.

لحفظ الخطوط في التدفقات بدلاً من الملفات ، استخدم ملحق[`FontStream`](./fontstream) منشأه.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->