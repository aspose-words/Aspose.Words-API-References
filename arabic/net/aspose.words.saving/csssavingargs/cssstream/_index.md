---
title: CssSavingArgs.CssStream
second_title: Aspose.Words لمراجع .NET API
description: CssSavingArgs ملكية. يسمح بتحديد الدفق الذي سيتم حفظ معلومات CSS فيه.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

يسمح بتحديد الدفق الذي سيتم حفظ معلومات CSS فيه.

```csharp
public Stream CssStream { get; set; }
```

### ملاحظات

تسمح لك هذه الخاصية بحفظ معلومات CSS في التدفق.

القيمة الافتراضية هي`باطل` . لا تمنع هذه الخاصية حفظ معلومات CSS في ملف أو تضمينها في مستند HTML. لمنع تصدير CSS، استخدم[`IsExportNeeded`](../isexportneeded/) ملكية.

استخدام[`ICssSavingCallback`](../../icsssavingcallback/) لا يمكنك استبدال CSS بـ آخر. الغرض منه هو حفظ CSS في الدفق فقط.

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


