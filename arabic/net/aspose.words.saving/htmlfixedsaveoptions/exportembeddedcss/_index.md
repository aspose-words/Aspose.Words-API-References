---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ExportEmbeddedCss في HtmlFixedSaveOptions مستندات HTML لديك عبر تضمين CSS لتصميم سلس. حسّن صفحات الويب الخاصة بك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

يحدد ما إذا كان يجب تضمين CSS (ورقة الأنماط المتتالية) في مستند HTML.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان تخزين أوراق أنماط CSS عند تصدير مستند إلى Html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// عندما نقوم بتصدير مستند إلى html، سيقوم Aspose.Words أيضًا بإنشاء ورقة أنماط CSS لتنسيق المستند بها.
// تعيين علامة "ExportEmbeddedCss" على "true" لحفظ ورقة أنماط CSS في ملف .css،
// وربط الملف من مستند html باستخدام عنصر <link>.
// سيؤدي تعيين العلم إلى "خطأ" إلى تضمين ورقة أنماط CSS داخل مستند HTML،
// والذي سوف يقوم بإنشاء ملف واحد فقط بدلا من ملفين.
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
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
