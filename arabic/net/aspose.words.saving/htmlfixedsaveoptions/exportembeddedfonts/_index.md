---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words لـ .NET
description: تحكّم بتضمين الخطوط في HTML باستخدام خاصية ExportEmbeddedFonts. حسّن جودة المستند مع إدارة حجمه بفعالية.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

يحدد ما إذا كان يجب تضمين الخطوط في مستند HTML بتنسيق Base64. لاحظ أن تعيين هذا العلم يمكن أن يزيد بشكل كبير من حجم ملف HTML الناتج.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان تخزين الخطوط المضمنة عند تصدير مستند إلى HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// عندما نقوم بتصدير مستند يحتوي على خطوط مضمنة إلى .html،
// يمكن لـ Aspose.Words وضع الخطوط في موقعين محتملين.
// سيؤدي تعيين علامة "ExportEmbeddedFonts" إلى "true" إلى تخزين البيانات الخام للخطوط المضمنة داخل ورقة أنماط CSS،
// في خاصية "url" لقاعدة "@font-face". قد يُنشئ هذا ملفًا ضخمًا لجدول أنماط CSS.
// وتقليل عدد الملفات الخارجية التي سيتم إنشاءها بواسطة تحويل HTML هذا.
// سيؤدي تعيين هذا العلم إلى "خطأ" إلى إنشاء ملف لكل خط.
// سوف تقوم ورقة أنماط CSS بالربط بكل ملف خط باستخدام خاصية "url" لقاعدة "@font-face".
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
