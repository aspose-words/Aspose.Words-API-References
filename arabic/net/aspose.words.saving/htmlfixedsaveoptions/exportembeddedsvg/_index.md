---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
second_title: Aspose.Words لمراجع .NET API
description: HtmlFixedSaveOptions ملكية. يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هيحقيقي .
type: docs
weight: 70
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

يحدد ما إذا كان يجب تضمين موارد SVG في مستند Html. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

### أمثلة

يوضح كيفية تحديد مكان تخزين كائنات SVG عند تصدير مستند إلى Html.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// عندما نقوم بتصدير مستند يحتوي على كائنات SVG إلى ‎.html،
// يمكن لـ Aspose.Words وضع هذه الكائنات في موقعين محتملين.
// سيؤدي تعيين علامة "ExportEmbeddedSvg" على "true" إلى تضمين كافة البيانات الأولية لكائن SVG
// داخل HTML الناتج، داخل <image> العلامات.
// سيؤدي تعيين هذه العلامة إلى "خطأ" إلى إنشاء ملف في نظام الملفات المحلي لكل كائن SVG.
// سوف يرتبط HTML بكل ملف باستخدام سمة "البيانات" الخاصة بالكائن <object> بطاقة شعار.
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
* مساحة الاسم [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* المجسم [Aspose.Words](../../../)


