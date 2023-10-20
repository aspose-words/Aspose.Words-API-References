---
title: PdfCustomPropertiesExport Enum
linktitle: PdfCustomPropertiesExport
articleTitle: PdfCustomPropertiesExport
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfCustomPropertiesExport تعداد. يحدد الطريقCustomDocumentProperties يتم تصديرها إلى ملف PDF في C#.
type: docs
weight: 5420
url: /ar/net/aspose.words.saving/pdfcustompropertiesexport/
---
## PdfCustomPropertiesExport enumeration

يحدد الطريق[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) يتم تصديرها إلى ملف PDF.

```csharp
public enum PdfCustomPropertiesExport
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لم يتم تصدير أي خصائص مخصصة. |
| Standard | `1` | يتم تصدير الخصائص المخصصة كإدخالات في قاموس /Info. |
| Metadata | `2` | الخصائص المخصصة هي بيانات التعريف. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
