---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.PdfCustomPropertiesExport على تعزيز تصدير PDF من خلال تخصيص خصائص المستند للحصول على أفضل النتائج.
type: docs
weight: 6210
url: /ar/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

يحدد الطريقة[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم تصدير أي خصائص مخصصة. |
| Standard | `1` | يتم تصدير الخصائص المخصصة كإدخالات في قاموس /Info. |
| Metadata | `2` | الخصائص المخصصة هي بيانات تعريفية. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
