---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ExportEmbeddedImages في HtmlFixedSaveOptions على تحسين مستندات HTML الخاصة بك عن طريق تضمين الصور بتنسيق Base64، وتحسين جودة الصورة أثناء إدارة حجم الملف.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

يحدد ما إذا كان يجب تضمين الصور في مستند HTML بتنسيق Base64. لاحظ أن تعيين هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف HTML الناتج.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان تخزين الصور عند تصدير مستند إلى HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// عندما نقوم بتصدير مستند يحتوي على صور مضمنة إلى .html،
// يمكن لـ Aspose.Words وضع الصور في موقعين محتملين.
// سيؤدي تعيين علامة "ExportEmbeddedImages" إلى "true" إلى تخزين البيانات الخام
// لجميع الصور الموجودة ضمن مستند HTML الناتج، في سمة "src" من علامات <image>.
// سيؤدي تعيين هذا العلم إلى "خطأ" إلى إنشاء ملف صورة في نظام الملفات المحلي لكل صورة،
// وتخزين كل هذه الملفات في مجلد منفصل.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
