---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.PdfFontEmbeddingMode لتضمين الخطوط بشكل مثالي في ملفات PDF. حسّن جودة المستندات وضمن عرضًا متناسقًا للنصوص.
type: docs
weight: 6260
url: /ar/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

يحدد كيفية تضمين الخطوط في Aspose.Words.

```csharp
public enum PdfFontEmbeddingMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmbedAll | `0` | يقوم Aspose.Words بتضمين جميع الخطوط. |
| EmbedNonstandard | `1` | يقوم Aspose.Words بتضمين جميع الخطوط باستثناء خطوط Windows القياسية Arial وTimes New Roman. تتأثر خطوط Arial وTimes New Roman فقط في هذا الوضع لأن MS Word لا يقوم بتضمين هذه الخطوط فقط عند حفظ المستند بتنسيق PDF. |
| EmbedNone | `2` | Aspose.Words لا تتضمن أي خطوط. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
