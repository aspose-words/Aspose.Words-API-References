---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ خيارات حفظ ملفات Pdf، المُصمم لتهيئة مستنداتك وحفظها بسهولة بتنسيق PDF عالي الجودة. بسّط سير عملك اليوم!
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

يقوم بتهيئة مثيل جديد لهذه الفئة التي يمكن استخدامها لحفظ مستند في Pdf تنسيق.

```csharp
public PdfSaveOptions()
```

## أمثلة

يوضح كيفية تمكين أو تعطيل التحديد الفرعي عند تضمين الخطوط أثناء عرض مستند بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بتكوين مصادر الخطوط لدينا للتأكد من أن لدينا إمكانية الوصول إلى كلا الخطوط في هذه الوثيقة.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// نظرًا لأن مستندنا يحتوي على خط مخصص، فقد يكون تضمينه في مستند الإخراج أمرًا مرغوبًا فيه.
// قم بضبط خاصية "EmbedFullFonts" على "true" لتضمين كل حرف من كل الخطوط المضمنة في ملف PDF الناتج.
// قد يصبح حجم المستند كبيرًا جدًا، ولكن سيكون لدينا استخدام كامل لجميع الخطوط إذا قمنا بتحرير ملف PDF.
// اضبط خاصية "EmbedFullFonts" على "false" لتطبيق التحديد الفرعي على الخطوط، مع حفظ الحروف فقط
// الذي يستخدمه المستند. سيكون حجم الملف أصغر بكثير،
// ولكن قد نحتاج إلى الوصول إلى أي خطوط مخصصة إذا قمنا بتحرير المستند.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

//استعادة مصادر الخط الأصلية.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
