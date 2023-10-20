---
title: PdfImageColorSpaceExportMode Enum
linktitle: PdfImageColorSpaceExportMode
articleTitle: PdfImageColorSpaceExportMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfImageColorSpaceExportMode تعداد. يحدد كيفية تحديد مساحة اللون للصور في مستند PDF في C#.
type: docs
weight: 5480
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
| Auto | `0` | يقوم Aspose.Words تلقائيًا بتحديد مساحة الألوان الأكثر ملاءمة لكل صورة. |
| SimpleCmyk | `1` | Aspose.Words يغطي صور RGB إلى مساحة ألوان CMYK باستخدام صيغة بسيطة. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
