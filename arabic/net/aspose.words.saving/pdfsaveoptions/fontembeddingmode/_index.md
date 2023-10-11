---
title: PdfSaveOptions.FontEmbeddingMode
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يحدد وضع تضمين الخط.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

يحدد وضع تضمين الخط.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيEmbedAll.

يعمل هذا الإعداد فقط مع النص بتشفير ANSI (Windows-1252). إذا كانت الوثيقة تحتوي على نص غير ANSI، فسيتم تضمين الخطوط المقابلة بغض النظر عن هذا الإعداد.

يتطلب التوافق مع PDF/A وPDF/UA تضمين جميع الخطوط. EmbedAll سيتم استخدام القيمة تلقائيًا عند الحفظ في PDF/A وPDF/UA.

### أمثلة

يوضح كيفية ضبط Aspose.Words لتخطي تضمين خطوط Arial وTimes New Roman في مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" هو خط قياسي، و"Courier New" هو خط غير قياسي.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "EmbedFullFonts" على "صحيح" لتضمين كل حرف رسومي لكل خط مضمن في ملف PDF الناتج.
options.EmbedFullFonts = true;

// قم بتعيين خاصية "FontEmbeddingMode" على "EmbedAll" لتضمين جميع الخطوط في ملف PDF الناتج.
// قم بتعيين خاصية "FontEmbeddingMode" على "EmbedNonstandard" للسماح فقط بتضمين الخطوط غير القياسية في ملف PDF الناتج.
// قم بتعيين خاصية "FontEmbeddingMode" على "EmbedNone" لعدم تضمين أي خطوط في ملف PDF الناتج.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### أنظر أيضا

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


