---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية التوافق مع PdfSaveOptions لضمان أن مستندات PDF الخاصة بك تلبي معايير الصناعة الخاصة بالجودة والتوافق.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

يحدد مستوى التوافق مع معايير PDF للمستندات الناتجة.

```csharp
public PdfCompliance Compliance { get; set; }
```

## ملاحظات

الافتراضي هوPdf17.

## أمثلة

يوضح كيفية تعيين مستوى التوافق مع معايير PDF للمستندات PDF المحفوظة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// لاحظ أن بعض خيارات حفظ PdfSaveOptions محظورة عند الحفظ إلى أحد المعايير ويتم إصلاحها تلقائيًا.
// استخدم IWarningCallback لمعرفة الخيارات التي تم إصلاحها تلقائيًا.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "التوافق" على "PdfCompliance.PdfA1b" للامتثال لمعيار "PDF/A-1b"،
// والذي يهدف إلى الحفاظ على المظهر المرئي للمستند حيث يقوم Aspose.Words بتحويله إلى PDF.
// قم بضبط خاصية "التوافق" إلى "PdfCompliance.Pdf17" للامتثال للمعيار "1.7".
// اضبط خاصية "التوافق" على "PdfCompliance.PdfA1a" للامتثال لمعيار "PDF/A-1a"،
// والذي يتوافق مع "PDF/A-1b" بالإضافة إلى الحفاظ على بنية المستند الأصلي.
// اضبط خاصية "التوافق" على "PdfCompliance.PdfUa1" للامتثال لمعيار "PDF/UA-1" (ISO 14289-1)،
// والتي تهدف إلى تحديد تمثيل المستندات الإلكترونية في PDF والتي تسمح بالوصول إلى الملف.
// قم بضبط خاصية "التوافق" إلى "PdfCompliance.Pdf20" للامتثال لمعيار "PDF 2.0" (ISO 32000-2).
// اضبط خاصية "التوافق" على "PdfCompliance.PdfA4" للامتثال لمعيار "PDF/A-4" (ISO 19004:2020)،
// الذي يحافظ على المظهر المرئي الثابت للمستند بمرور الوقت.
// اضبط خاصية "التوافق" على "PdfCompliance.PdfA4Ua2" للتوافق مع كل من PDF/A-4 (ISO 19005-4:2020)
// ومعايير PDF/UA-2 (ISO 14289-2:2024).
// قم بضبط خاصية "التوافق" إلى "PdfCompliance.PdfUa2" للامتثال لمعيار PDF/UA-2 (ISO 14289-2:2024).
// يساعد هذا في جعل المستندات قابلة للبحث ولكن قد يؤدي إلى زيادة كبيرة في حجم المستندات الكبيرة بالفعل.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
