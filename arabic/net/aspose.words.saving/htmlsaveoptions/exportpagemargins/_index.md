---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية HtmlSaveOptions ExportPageMargins على تعزيز صادرات HTML وMHTML وEPUB من خلال التحكم في هوامش الصفحة للحصول على عرض تقديمي أنيق.
type: docs
weight: 210
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

يحدد ما إذا كان سيتم تصدير هوامش الصفحة إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportPageMargins { get; set; }
```

## ملاحظات

لا يعرض Aspose.Words مساحة هوامش الصفحة بشكل افتراضي. إذا تم اقتصاص أي عناصر بشكل كامل أو جزئي بواسطة حافة المستند، فيمكن تمديد المساحة المعروضة باستخدام هذا الخيار.

## أمثلة

يوضح كيفية إظهار الكائنات خارج الحدود في مستندات HTML الناتجة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم المنشئ لإدراج شكل بدون التفاف.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// قد تؤدي قيم موضع الشكل السلبية إلى وضع الشكل خارج حدود الصفحة.
// إذا قمنا بتصدير هذا إلى HTML، سيظهر الشكل مقطوعًا.
shape.Left = -150;

// عند حفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// لتحديد ما إذا كان سيتم تعديل الصفحة لعرض الكائنات خارج الحدود بالكامل.
// إذا قمنا بتعيين علم "ExportPageMargins" إلى "true"، فسيكون الشكل مرئيًا بالكامل في HTML الناتج.
// إذا قمنا بتعيين علامة "ExportPageMargins" إلى "false"،
// سوف يعرض مستندنا الشكل مقطوعًا كما نراه في Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
