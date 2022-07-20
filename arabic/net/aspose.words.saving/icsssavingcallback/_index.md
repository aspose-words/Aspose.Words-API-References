---
title: ICssSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ CSS ورقة الأنماط المتتالية عند حفظ مستند إلى HTML.
type: docs
weight: 4870
url: /ar/net/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية قيام Aspose.Words بحفظ CSS (ورقة الأنماط المتتالية) عند حفظ مستند إلى HTML.

```csharp
public interface ICssSavingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [CssSaving](../../aspose.words.saving/icsssavingcallback/csssaving)(CssSavingArgs) | يتم استدعاؤها عند قيام Aspose.Words بحفظ CSS (ورقة الأنماط المتتالية) ._ x000d_ |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->