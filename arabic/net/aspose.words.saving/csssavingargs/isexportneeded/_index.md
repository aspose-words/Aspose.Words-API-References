---
title: CssSavingArgs.IsExportNeeded
second_title: Aspose.Words لمراجع .NET API
description: CssSavingArgs ملكية. يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف ودمجه في مستند HTML. الافتراضي هوحقيقي . عندما تكون هذه الخاصيةخطأ شنيع  لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينها في مستند HTML.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/csssavingargs/isexportneeded/
---
## CssSavingArgs.IsExportNeeded property

يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف ودمجه في مستند HTML. الافتراضي هو`حقيقي` . عندما تكون هذه الخاصية`خطأ شنيع` ، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينها في مستند HTML.

```csharp
public bool IsExportNeeded { get; set; }
```

### أمثلة

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

* class [CssSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../csssavingargs/)
* المجسم [Aspose.Words](../../../)


