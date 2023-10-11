---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
second_title: Aspose.Words لمراجع .NET API
description: HtmlFixedSaveOptions ملكية. يحدد ما إذا كان يجب تضمين CSS ورقة الأنماط المتتالية في مستند Html.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

يحدد ما إذا كان يجب تضمين CSS (ورقة الأنماط المتتالية) في مستند Html.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

### أمثلة

يوضح كيفية تحديد مكان تخزين أوراق أنماط CSS عند تصدير مستند إلى Html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بتصدير مستند إلى html، سيقوم Aspose.Words أيضًا بإنشاء ورقة أنماط CSS لتنسيق المستند بها.
// ضبط علامة "ExportEmbeddedCss" على "صحيح" وحفظ ورقة أنماط CSS في ملف ‎.css،
// واربط الملف من مستند html باستخدام <link> عنصر.
// سيؤدي تعيين العلامة إلى "خطأ" إلى تضمين ورقة أنماط CSS داخل مستند Html،
// والذي سيؤدي إلى إنشاء ملف واحد فقط بدلاً من ملفين.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


