---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfFontEmbeddingMode تعداد. يحدد كيفية قيام Aspose.Words بتضمين الخطوط في C#.
type: docs
weight: 5470
url: /ar/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

يحدد كيفية قيام Aspose.Words بتضمين الخطوط.

```csharp
public enum PdfFontEmbeddingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words يدمج كافة الخطوط. |
| EmbedNonstandard | `1` | يقوم Aspose.Words بتضمين جميع الخطوط باستثناء خطوط Windows القياسية Arial وTimes New Roman. تتأثر خطوط Arial وTimes New Roman فقط في هذا الوضع لأن MS Word لا يقوم بتضمين هذه الخطوط فقط عند حفظ المستند إلى PDF. |
| EmbedNone | `2` | Aspose.Words لا تتضمن أي خطوط. |

## أمثلة

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
