---
title: PdfSaveOptions.EmbedFullFonts
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة.
type: docs
weight: 120
url: /ar/net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

يتحكم في كيفية تضمين الخطوط في مستندات PDF الناتجة.

```csharp
public bool EmbedFullFonts { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع`، مما يعني أنه تم تعيين الخطوط فرعيًا قبل التضمين. يعد الإعداد الفرعي مفيدًا إذا كنت تريد الاحتفاظ بحجم ملف الإخراج أصغر. يؤدي الإعداد الفرعي إلى إزالة جميع الحروف الرسومية غير المستخدمة من الخط.

عندما يتم ضبط هذه القيمة على`حقيقي`، يتم تضمين ملف خط كامل في PDF بدون إعدادات فرعية. سيؤدي هذا إلى إخراج ملفات أكبر، ولكن يمكن أن يكون خيارًا مفيدًا عندما تريد تحرير ملف PDF الناتج لاحقًا (على سبيل المثال، إضافة المزيد من النص).

بعض الخطوط كبيرة الحجم (عدة ميغابايت) وسيؤدي تضمينها بدون subsetting إلى إنتاج مستندات كبيرة الحجم.

### أمثلة

يوضح كيفية تمكين الإعداد الفرعي أو تعطيله عند تضمين الخطوط أثناء عرض مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// قم بتكوين مصادر الخطوط لدينا للتأكد من أننا نستطيع الوصول إلى كلا الخطين في هذه الوثيقة.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource = new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// نظرًا لأن وثيقتنا تحتوي على خط مخصص، فقد يكون التضمين في مستند الإخراج أمرًا مرغوبًا فيه.
// اضبط خاصية "EmbedFullFonts" على "صحيح" لتضمين كل حرف رسومي لكل خط مضمن في ملف PDF الناتج.
// قد يصبح حجم المستند كبيرًا جدًا، ولكن سيكون لدينا الاستخدام الكامل لجميع الخطوط إذا قمنا بتحرير ملف PDF.
// قم بتعيين خاصية "EmbedFullFonts" على "خطأ" لتطبيق الإعداد الفرعي على الخطوط، مع حفظ الحروف الرسومية فقط
// الذي يستخدمه المستند. سيكون الملف أصغر بكثير،
// لكننا قد نحتاج إلى الوصول إلى أي خطوط مخصصة إذا قمنا بتحرير المستند.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

if (embedFullFonts)
    Assert.That(500000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));
else
    Assert.That(25000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf").Length));

// استعادة مصادر الخط الأصلي.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


