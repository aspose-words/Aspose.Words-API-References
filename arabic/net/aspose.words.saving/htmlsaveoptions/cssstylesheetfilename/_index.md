---
title: HtmlSaveOptions.CssStyleSheetFileName
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد المسار واسم ملف ورقة الأنماط المتتالية CSS المكتوب عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

يحدد المسار واسم ملف ورقة الأنماط المتتالية (CSS) المكتوب عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string CssStyleSheetFileName { get; set; }
```

### ملاحظات

هذه الخاصية لها تأثير فقط عند حفظ مستند بتنسيق HTML ويتم طلب ورقة أنماط CSS خارجية باستخدام[`CssStyleSheetType`](../cssstylesheettype/).

إذا كانت هذه الخاصية فارغة ، فسيتم حفظ ملف CSS في نفس المجلد وبنفس اسم مستند HTML ولكن بامتداد ".css".

إذا تم تحديد مسار فقط ولكن لم يتم تحديد اسم ملف في هذه الخاصية ، فسيتم حفظ ملف CSS في المجلد المحدد وسيكون له نفس اسم مستند HTML ولكن بامتداد ".css".

إذا كان المجلد المحدد بواسطة هذه الخاصية غير موجود ، فسيتم إنشاؤه تلقائيًا قبل حفظ ملف CSS file .

هناك طريقة أخرى لتحديد مجلد حيث يتم حفظ ملف CSS خارجي وهي استخدام[`ResourceFolder`](../resourcefolder/) .

### أمثلة

يوضح كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // قم بإنشاء كائن "HtmlFixedSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // عيّن الخاصية "CssStylesheetType" على "CssStyleSheetType.External" على
    // إرفاق مستند HTML محفوظ بملف ورقة أنماط CSS خارجي.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // فيما يلي طريقتان لتحديد الدلائل وأسماء الملفات لأوراق أنماط الإخراج CSS.
    // 1 - استخدم خاصية "CssStyleSheetFileName" لتعيين اسم ملف إلى ورقة الأنماط الخاصة بنا:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - استخدم رد اتصال مخصص لتسمية ورقة الأنماط الخاصة بنا:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// يعين اسم ملف مخصص ، مع معلمات أخرى لورقة أنماط CSS خارجية.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // يمكننا الوصول إلى المستند المصدر بالكامل عبر خاصية "المستند".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


