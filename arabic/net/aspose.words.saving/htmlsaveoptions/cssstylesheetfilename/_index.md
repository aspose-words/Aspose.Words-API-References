---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions CssStyleSheetFileName ملكية. يحدد المسار واسم ملف ورقة الأنماط المتتالية CSS الذي يتم كتابته عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

يحدد المسار واسم ملف ورقة الأنماط المتتالية (CSS) الذي يتم كتابته عند تصدير مستند إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## ملاحظات

تكون هذه الخاصية سارية فقط عند حفظ مستند بتنسيق HTML وطلب ورقة أنماط CSS خارجية باستخدام[`CssStyleSheetType`](../cssstylesheettype/).

إذا كانت هذه الخاصية فارغة، فسيتم حفظ ملف CSS في نفس المجلد وبنفس اسم مستند HTML ولكن بامتداد ".css".

إذا تم تحديد مسار فقط ولكن لم يتم تحديد اسم ملف في هذه الخاصية، فسيتم حفظ ملف CSS في المجلد المحدد وسيكون له نفس اسم مستند HTML ولكن بامتداد ".css".

إذا كان المجلد المحدد بهذه الخاصية غير موجود، فسيتم إنشاؤه تلقائيًا قبل حفظ ملف CSS file .

هناك طريقة أخرى لتحديد المجلد الذي يتم حفظ ملف CSS الخارجي فيه وهي الاستخدام[`ResourceFolder`](../resourcefolder/) .

## أمثلة

يوضح كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // قم بتعيين خاصية "CssStylesheetType" على "CssStyleSheetType.External" إلى
    // قم بإرفاق مستند HTML محفوظ بملف ورقة أنماط CSS خارجي.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // فيما يلي طريقتان لتحديد الدلائل وأسماء الملفات لأوراق أنماط CSS الناتجة.
    // 1 - استخدم خاصية "CssStyleSheetFileName" لتعيين اسم ملف لورقة الأنماط الخاصة بنا:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - استخدم رد اتصال مخصصًا لتسمية ورقة الأنماط الخاصة بنا:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// يعين اسم ملف مخصصًا، بالإضافة إلى معلمات أخرى لورقة أنماط CSS خارجية.
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
        // يمكننا الوصول إلى المستند المصدر بأكمله عبر خاصية "المستند".
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
