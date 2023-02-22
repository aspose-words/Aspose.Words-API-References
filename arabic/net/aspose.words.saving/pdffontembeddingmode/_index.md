---
title: Enum PdfFontEmbeddingMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfFontEmbeddingMode تعداد. يحدد كيفية قيام Aspose.Words بتضمين الخطوط .
type: docs
weight: 5190
url: /ar/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

يحدد كيفية قيام Aspose.Words بتضمين الخطوط .

```csharp
public enum PdfFontEmbeddingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words بتضمين كل الخطوط . |
| EmbedNonstandard | `1` | Aspose.Words بتضمين جميع الخطوط باستثناء خطوط Windows القياسية Arial و Times New Roman . تتأثر خطوط Arial و Times New Roman فقط في هذا الوضع لأن MS Word لا يدمج هذه الخطوط فقط عند حفظ المستند في PDF . |
| EmbedNone | `2` | Aspose. لا تتضمن الكلمات أي خطوط . |

### أمثلة

يوضح كيفية تعيين Aspose.Words لتخطي دمج خطوط Arial و Times New Roman في مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" خط قياسي ، و "Courier New" خط غير قياسي.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "EmbedFullFonts" على "true" لتضمين كل حرف رسومي لكل خط مضمن في ملف PDF الناتج.
options.EmbedFullFonts = true;

// اضبط خاصية "FontEmbeddingMode" على "EmbedAll" لتضمين كل الخطوط في ملف PDF الناتج.
// اضبط خاصية "FontEmbeddingMode" على "EmbedNonstandard" للسماح فقط بدمج الخطوط غير القياسية في ملف PDF الناتج.
// اضبط خاصية "FontEmbeddingMode" على "EmbedNone" لعدم تضمين أي خطوط في ملف PDF الناتج.
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
        Assert.That(4217, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


