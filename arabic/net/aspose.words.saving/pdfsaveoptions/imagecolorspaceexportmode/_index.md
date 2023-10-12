---
title: PdfSaveOptions.ImageColorSpaceExportMode
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يحدد كيفية تحديد مساحة اللون للصور في مستند PDF.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

يحدد كيفية تحديد مساحة اللون للصور في مستند PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيAuto .

إذاSimpleCmyk تم تحديد القيمة، [`ImageCompression`](../imagecompression/) يتم تجاهل الخيار و يتم استخدام ضغط Flate لجميع الصور الموجودة في المستند.

SimpleCmyk القيمة غير مدعومة عند الحفظ بتنسيق PDF/A. Auto سيتم استخدام القيمة بدلاً من ذلك.

### أمثلة

يوضح كيفية تعيين مساحة ألوان مختلفة للصور في مستند أثناء تصديره إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.Auto" للحصول على Aspose.Words
// تحديد مساحة اللون تلقائيًا للصور الموجودة في المستند الذي يقوم بتحويله إلى PDF.
// في معظم الحالات، ستكون مساحة اللون RGB.
// قم بتعيين خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.SimpleCmyk"
// لاستخدام مساحة ألوان CMYK لجميع الصور في ملف PDF المحفوظ.
// Aspose.Words سيطبق أيضًا ضغط Flate على جميع الصور ويتجاهل قيمة خاصية "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### أنظر أيضا

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


