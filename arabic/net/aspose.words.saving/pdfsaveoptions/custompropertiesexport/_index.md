---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PdfSaveOptions CustomPropertiesExport على تعزيز صادرات PDF الخاصة بك عن طريق التحكم في CustomDocumentProperties للحصول على أفضل النتائج.
type: docs
weight: 70
url: /ar/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

يحصل على قيمة تحدد الطريقة أو يعينها[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone.

Metadata القيمة غير مدعومة عند الحفظ بتنسيق PDF/A. Standard سيتم استخدامه بدلاً من PDF/A-1 وPDF/A-2 و None لملف PDF/A-4.

Standard القيمة غير مدعومة عند الحفظ في PDF 2.0. Metadata سيتم استخدامها بدلا من ذلك.

## أمثلة

يوضح كيفية تصدير الخصائص المخصصة أثناء تحويل مستند إلى PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.None" للتخلص منها
// خصائص المستند المخصصة أثناء حفظ المستند بتنسيق .PDF.
// اضبط خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.Standard"
// للحفاظ على الخصائص المخصصة داخل مستند PDF الناتج.
// اضبط خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.Metadata"
// للحفاظ على الخصائص المخصصة في حزمة XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### أنظر أيضا

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
