---
title: HtmlSaveOptions.ExportPageMargins
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان سيتم تصدير هوامش الصفحة إلى HTML أو MHTML أو EPUB . الافتراضي هوخاطئة .
type: docs
weight: 220
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

يحدد ما إذا كان سيتم تصدير هوامش الصفحة إلى HTML أو MHTML أو EPUB . الافتراضي هو`خاطئة` .

```csharp
public bool ExportPageMargins { get; set; }
```

### ملاحظات

Aspose.Words لا يُظهر هوامش الصفحة افتراضيًا. إذا تم قص أي عناصر كليًا أو جزئيًا بواسطة حافة المستند ، فيمكن تمديد المنطقة المعروضة باستخدام هذا الخيار .

### أمثلة

يوضح كيفية إظهار الكائنات خارج الحدود في مستندات HTML الناتجة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم أداة إنشاء لإدراج شكل بدون التفاف.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// قد تضع قيم موضع الشكل السلبية الشكل خارج حدود الصفحة.
// إذا قمنا بتصدير هذا إلى HTML ، فسيظهر الشكل مقطوعًا.
shape.Left = -150;

// عند حفظ المستند إلى HTML ، يمكننا تمرير كائن SaveOptions
// لتقرر ما إذا كنت تريد ضبط الصفحة لعرض الكائنات خارج الحدود بالكامل.
// إذا قمنا بتعيين علامة "ExportPageMargins" على "true" ، فسيكون الشكل مرئيًا بالكامل في HTML الناتج.
// إذا قمنا بتعيين علامة "ExportPageMargins" على "خطأ" ،
// سيعرض وثيقتنا الشكل المقطوع كما نراه في Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section1\"><p style=\"margin-top:0pt; margin-left:151pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:221.85pt; margin-bottom:0pt\">"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


