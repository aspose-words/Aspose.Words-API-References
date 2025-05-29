---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontEmbeddingMode في PdfSaveOptions لتحسين تضمين الخطوط في ملف PDF. حسّن جودة المستند وتوافقه بسهولة!
type: docs
weight: 170
url: /ar/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

يحدد وضع تضمين الخط.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيEmbedAll.

يعمل هذا الإعداد فقط مع النص المُرمَّز بترميز ANSI (Windows-1252). إذا احتوى المستند على نص غير مُرمَّز بترميز ANSI، فسيتم تضمين الخطوط المُقابلة بغض النظر عن هذا الإعداد.

يتطلب التوافق مع PDF/A وPDF/UA تضمين جميع الخطوط. EmbedAll سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A وPDF/UA.

## أمثلة

يوضح كيفية إعداد Aspose.Words لتخطي تضمين الخطوط Arial وTimes New Roman في مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//"Arial" هو خط قياسي، و"Courier New" هو خط غير قياسي.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// قم بضبط خاصية "EmbedFullFonts" على "true" لتضمين كل حرف من كل الخطوط المضمنة في ملف PDF الناتج.
options.EmbedFullFonts = true;
// قم بتعيين خاصية "FontEmbeddingMode" إلى "EmbedAll" لتضمين جميع الخطوط في ملف PDF الناتج.
// قم بتعيين خاصية "FontEmbeddingMode" إلى "EmbedNonstandard" للسماح فقط بتضمين الخطوط غير القياسية في ملف PDF الناتج.
// قم بتعيين خاصية "FontEmbeddingMode" إلى "EmbedNone" لعدم تضمين أي خطوط في ملف PDF الناتج.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### أنظر أيضا

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
