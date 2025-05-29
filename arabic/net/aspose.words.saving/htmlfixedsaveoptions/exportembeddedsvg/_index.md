---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ExportEmbeddedSvg في HtmlFixedSaveOptions، وقم بتضمين موارد SVG بسهولة في مستندات HTML لتحسين جودة الصور. افتراضيًا، القيمة true.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

يحدد ما إذا كان يجب تضمين موارد SVG في مستند HTML. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان تخزين كائنات SVG عند تصدير مستند إلى Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// عندما نقوم بتصدير مستند يحتوي على كائنات SVG إلى .html،
// يمكن لـ Aspose.Words وضع هذه الكائنات في موقعين محتملين.
// سيؤدي تعيين علامة "ExportEmbeddedSvg" إلى "true" إلى تضمين جميع بيانات كائن SVG الخام
// داخل HTML الناتج، داخل علامات <image>.
// سيؤدي تعيين هذا العلم إلى "false" إلى إنشاء ملف في نظام الملفات المحلي لكل كائن SVG.
// سوف يقوم HTML بالربط بكل ملف باستخدام سمة "data" الخاصة بعلامة <object>.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
