---
title: PdfSaveOptions.ImageColorSpaceExportMode
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يحدد كيفية اختيار مساحة اللون للصور في مستند PDF.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/
---
## PdfSaveOptions.ImageColorSpaceExportMode property

يحدد كيفية اختيار مساحة اللون للصور في مستند PDF.

```csharp
public PdfImageColorSpaceExportMode ImageColorSpaceExportMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيAuto .

إذاSimpleCmyk تم تحديد القيمة ، [`ImageCompression`](../imagecompression/) يتم تجاهل الخيار و يتم استخدام ضغط Flate لجميع الصور في المستند.

SimpleCmyk القيمة غير مدعومة عند الحفظ في PDF / A. Auto سيتم استخدام القيمة بدلاً من ذلك.

### أمثلة

يوضح كيفية تعيين مساحة ألوان مختلفة للصور في مستند أثناء تصديرها إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// اضبط خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.Auto" للحصول على Aspose.Words إلى
// يحدد تلقائيًا مساحة اللون للصور في المستند الذي يتم تحويله إلى PDF.
// في معظم الحالات ، ستكون مساحة اللون هي RGB.
// تعيين خاصية "ImageColorSpaceExportMode" على "PdfImageColorSpaceExportMode.SimpleCmyk"
// لاستخدام مساحة ألوان CMYK لجميع الصور في PDF المحفوظ.
// Aspose.Words ستطبق أيضًا ضغط Flate على جميع الصور وتتجاهل قيمة خاصية "ImageCompression".
pdfSaveOptions.ImageColorSpaceExportMode = pdfImageColorSpaceExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
```

### أنظر أيضا

* enum [PdfImageColorSpaceExportMode](../../pdfimagecolorspaceexportmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


