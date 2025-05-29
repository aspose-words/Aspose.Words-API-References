---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words PdfImageColorSpaceExportMode لتحسين اختيار ألوان الصورة في مستندات PDF الخاصة بك للحصول على صور مذهلة.
type: docs
weight: 6270
url: /ar/net/aspose.words.saving/pdfimagecolorspaceexportmode/
---
## PdfImageColorSpaceExportMode enumeration

يحدد كيفية تحديد مساحة اللون للصور في مستند PDF.

```csharp
public enum PdfImageColorSpaceExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | يقوم Aspose.Words تلقائيًا باختيار مساحة اللون الأكثر ملاءمة لكل صورة. |
| SimpleCmyk | `1` | يقوم Aspose.Words بتحويل صور RGB إلى مساحة ألوان CMYK باستخدام صيغة بسيطة. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
