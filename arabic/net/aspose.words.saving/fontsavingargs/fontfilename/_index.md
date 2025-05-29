---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontSavingArgs FontFileName، وقم بإدارة أسماء ملفات الخطوط بسهولة وتعزيز سير عمل التصميم الخاص بك من خلال إمكانيات الحفظ السلسة.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

يحصل على اسم الملف (بدون مسار) الذي سيتم حفظ الخط فيه أو يعينه.

```csharp
public string FontFileName { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات الخطوط أثناء التصدير إلى HTML.

عند تشغيل الحدث، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words. يمكنك تغيير قيمة هذه الخاصية لحفظ الخط في ملف مختلف. يُرجى ملاحظة أن أسماء الملفات يجب أن تكون فريدة.

يُنشئ Aspose.Words تلقائيًا اسم ملف فريدًا لكل خط مُضمّن عند تصدير إلى تنسيق HTML. تعتمد طريقة إنشاء اسم ملف الخط على ما إذا كنت تحفظ المستند في ملف أم في مسار.

عند حفظ مستند في ملف، يبدو اسم ملف الخط الناتج مثل &lt;اسم ملف قاعدة المستند&gt;.&lt;اسم الملف الأصلي&gt;.لاحقة اختيارية&gt;.&lt;الامتداد&gt;.

عند حفظ مستند في مجرى، يبدو اسم ملف الخط الناتج مثل Aspose.Words.&lt;دليل المستند&gt;.&lt;اسم الملف الأصلي&gt;&lt;لاحقة اختيارية&gt;.&lt;الامتداد&gt;.

`FontFileName` يجب أن يحتوي فقط على اسم الملف بدون المسار. يحدد Aspose.Words المسار للحفظ باستخدام اسم ملف المستند، [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) و [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) ملكيات.

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
