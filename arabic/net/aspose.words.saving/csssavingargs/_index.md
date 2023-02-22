---
title: Class CssSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.CssSavingArgs فصل. توفير بيانات لملفCssSaving الحدث .
type: docs
weight: 4620
url: /ar/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

توفير بيانات لملف[`CssSaving`](../icsssavingcallback/csssaving/) الحدث .

```csharp
public class CssSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | يسمح بتحديد التدفق حيث سيتم حفظ معلومات CSS فيه. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | الحصول على كائن المستند الذي يتم حفظه حاليًا. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | يسمح بتحديد ما إذا كان سيتم تصدير CSS إلى ملف وتضمينه في مستند HTML. الافتراضي هو`حقيقي` . عندما تكون هذه الخاصية`خاطئة` ، لن يتم حفظ معلومات CSS في ملف CSS ولن يتم تضمينها في مستند HTML. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ معلومات CSS. |

### ملاحظات

بشكل افتراضي ، عندما يحفظ Aspose.Words مستند إلى HTML ، فإنه يحفظ معلومات CSS inline (كقيمة لـ **نمط** السمة على كل عنصر) .

`CssSavingArgs` يسمح بحفظ معلومات CSS في ملف من خلال توفير كائن البث الخاص بك.

لحفظ CSS في الدفق ، استخدم ملف[`CssStream`](./cssstream/) منشأه.

لمنع حفظ CSS في ملف والتضمين في مستند HTML ، استخدم الامتداد[`IsExportNeeded`](./isexportneeded/) منشأه.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


