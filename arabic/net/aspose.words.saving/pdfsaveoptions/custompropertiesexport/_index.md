---
title: PdfSaveOptions.CustomPropertiesExport
linktitle: CustomPropertiesExport
articleTitle: CustomPropertiesExport
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions CustomPropertiesExport ملكية. الحصول على أو تحديد قيمة تحدد الطريقCustomDocumentProperties يتم تصديرها إلى ملف PDF في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/pdfsaveoptions/custompropertiesexport/
---
## PdfSaveOptions.CustomPropertiesExport property

الحصول على أو تحديد قيمة تحدد الطريق[`CustomDocumentProperties`](../../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF.

```csharp
public PdfCustomPropertiesExport CustomPropertiesExport { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone.

Metadata القيمة غير مدعومة عند الحفظ بتنسيق PDF/A. Standard سيتم استخدامه بدلاً من ذلك لـ PDF/A-1 وPDF/A-2 و None لـ PDF/A-4.

Standard القيمة غير مدعومة عند الحفظ في PDF 2.0. Metadata سيتم استخدامها بدلا من ذلك.

## أمثلة

يوضح كيفية تصدير الخصائص المخصصة أثناء تحويل مستند إلى PDF.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("Company", "My value");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// قم بتعيين خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.None" للتجاهل
// خصائص الوثيقة المخصصة عندما نحفظ الوثيقة بصيغة PDF.
// قم بتعيين خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.Standard"
// للحفاظ على الخصائص المخصصة داخل مستند PDF الناتج.
// قم بتعيين خاصية "CustomPropertiesExport" على "PdfCustomPropertiesExport.Metadata"
// للحفاظ على الخصائص المخصصة في حزمة XMP.
options.CustomPropertiesExport = pdfCustomPropertiesExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
```

### أنظر أيضا

* enum [PdfCustomPropertiesExport](../../pdfcustompropertiesexport/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
