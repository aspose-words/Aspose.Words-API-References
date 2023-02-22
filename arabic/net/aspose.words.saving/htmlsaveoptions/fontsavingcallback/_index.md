---
title: HtmlSaveOptions.FontSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يسمح بالتحكم في كيفية حفظ الخطوط عند حفظ المستند بتنسيق HTML أو MHTML أو EPUB.
type: docs
weight: 310
url: /ar/net/aspose.words.saving/htmlsaveoptions/fontsavingcallback/
---
## HtmlSaveOptions.FontSavingCallback property

يسمح بالتحكم في كيفية حفظ الخطوط عند حفظ المستند بتنسيق HTML أو MHTML أو EPUB.

```csharp
public IFontSavingCallback FontSavingCallback { get; set; }
```

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

* interface [IFontSavingCallback](../../ifontsavingcallback/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


