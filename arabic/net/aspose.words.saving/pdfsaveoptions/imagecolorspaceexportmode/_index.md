---
title: PdfSaveOptions.ImageColorSpaceExportMode
linktitle: ImageColorSpaceExportMode
articleTitle: ImageColorSpaceExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions ImageColorSpaceExportMode لتحسين اختيار ألوان الصورة في ملفات PDF الخاصة بك للحصول على جودة بصرية مذهلة وتناسق.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

يحدد كيفية تحديد مساحة اللون للصور في مستند PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيAuto .

إذاSimpleCmyk تم تحديد القيمة، [`ImageCompression`](../imagecompression/) يتم تجاهل الخيار ويتم استخدام ضغط Flate لجميع الصور في المستند.

SimpleCmyk القيمة غير مدعومة عند الحفظ بتنسيق PDF/A. Auto سيتم استخدام القيمة بدلا من ذلك.

## أمثلة

يوضح كيفية تعيين مساحة ألوان مختلفة للصور في مستند أثناء تصديره إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// اضبط خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.Auto" للحصول على Aspose.Words إلى
// حدد تلقائيًا مساحة اللون للصور في المستند الذي يتم تحويله إلى PDF.
// في معظم الحالات، ستكون مساحة اللون RGB.
// اضبط خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.SimpleCmyk"
// لاستخدام مساحة ألوان CMYK لجميع الصور الموجودة في ملف PDF المحفوظ.
// سوف يقوم Aspose.Words أيضًا بتطبيق ضغط Flate على جميع الصور ويتجاهل قيمة خاصية "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### أنظر أيضا

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
