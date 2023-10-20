---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.CssStyleSheetType تعداد. يحدد كيفية تصدير أنماط CSS ورقة الأنماط المتتالية إلى HTML في C#.
type: docs
weight: 4890
url: /ar/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

يحدد كيفية تصدير أنماط CSS (ورقة الأنماط المتتالية) إلى HTML.

```csharp
public enum CssStyleSheetType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Inline | `0` | تتم كتابة أنماط CSS بشكل مضمن (كقيمة لـ**أسلوب** سمة على كل عنصر). |
| Embedded | `1` | تتم كتابة أنماط CSS بشكل منفصل عن المحتوى في ورقة الأنماط المضمنة في ملف HTML. |
| External | `2` | تتم كتابة أنماط CSS بشكل منفصل عن المحتوى الموجود في ورقة الأنماط في ملف خارجي. يربط ملف HTML ورقة الأنماط. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
