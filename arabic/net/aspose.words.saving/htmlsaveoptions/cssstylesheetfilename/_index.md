---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم خاصية HtmlSaveOptions CssStyleSheetFileName بتخصيص صادرات HTML الخاصة بك باستخدام مسار ملف CSS محدد، مما يعزز أسلوب مستندك.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

يحدد المسار واسم ملف Cascading Style Sheet (CSS) المكتوب عند تصدير document إلى HTML. الافتراضي هو سلسلة فارغة.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## ملاحظات

لا يكون لهذه الخاصية تأثير إلا عند حفظ مستند بتنسيق HTML ويتم طلب ورقة أنماط CSS خارجية باستخدام[`CssStyleSheetType`](../cssstylesheettype/).

إذا كانت هذه الخاصية فارغة، سيتم حفظ ملف CSS في نفس المجلد وبنفس اسم مستند HTML ولكن مع الامتداد ".css".

إذا تم تحديد المسار فقط ولكن لم يتم تحديد اسم الملف في هذه الخاصية، فسيتم حفظ ملف CSS في المجلد selected وسيكون له نفس اسم مستند HTML ولكن مع امتداد ".css".

إذا لم يكن المجلد المحدد بواسطة هذه الخاصية موجودًا، فسيتم إنشاؤه تلقائيًا قبل حفظ ملف CSS file .

هناك طريقة أخرى لتحديد المجلد الذي سيتم حفظ ملف CSS الخارجي فيه وهي استخدام[`ResourceFolder`](../resourcefolder/) .

## أمثلة

يوضح كيفية العمل مع أوراق أنماط CSS التي ينشئها تحويل HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // اضبط خاصية "CssStylesheetType" إلى "CssStyleSheetType.External"
    // قم بإرفاق مستند HTML المحفوظ بملف جدول أنماط CSS خارجي.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // فيما يلي طريقتان لتحديد الدلائل وأسماء الملفات لأوراق أنماط CSS الناتجة.
    // 1 - استخدم خاصية "CssStyleSheetFileName" لتعيين اسم ملف لورقة الأنماط الخاصة بنا:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - استخدم استدعاء مخصص لتسمية ورقة الأنماط الخاصة بنا:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// تعيين اسم ملف مخصص، إلى جانب معلمات أخرى لنمط CSS الخارجي.
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
        //يمكننا الوصول إلى المستند المصدر بأكمله عبر خاصية "المستند".
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
