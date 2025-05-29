---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل ميزة PdfSaveOptions EmbedFullFonts على تعزيز مستندات PDF الخاصة بك من خلال ضمان تضمين الخط بالكامل للحصول على تنسيق مثالي.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة.

```csharp
public bool EmbedFullFonts { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`، مما يعني أن الخطوط تُحذف قبل التضمين. يُعد حذف مفيدًا إذا كنت ترغب في تقليل حجم ملف الإخراج. يزيل حذف جميع الرموز غير المستخدمة من الخط.

عندما يتم تعيين هذه القيمة على`حقيقي`يتم تضمين ملف خط كامل في ملف PDF دون أي تعديلات. سيؤدي هذا إلى إنتاج ملفات إخراج أكبر، ولكنه قد يكون خيارًا مفيدًا عند الرغبة في تعديل ملف PDF الناتج لاحقًا (مثل إضافة نص إضافي).

بعض الخطوط كبيرة الحجم (عدة ميغا بايت) وتضمينها بدون subsetting سيؤدي إلى إنتاج مستندات إخراج كبيرة الحجم.

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
