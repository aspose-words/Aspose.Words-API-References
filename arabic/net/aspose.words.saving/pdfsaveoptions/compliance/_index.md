---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions Compliance ملكية. يحدد مستوى التوافق مع معايير PDF لمستندات المخرجات في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

يحدد مستوى التوافق مع معايير PDF لمستندات المخرجات.

```csharp
public PdfCompliance Compliance { get; set; }
```

## ملاحظات

الافتراضي هوPdf17.

## أمثلة

يوضح كيفية تعيين مستوى الامتثال لمعايير PDF لمستندات PDF المحفوظة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
// لاحظ أن بعض خيارات PdfSaveOptions محظورة عند الحفظ في أحد المعايير ويتم إصلاحها تلقائيًا.
// استخدم IWarningCallback لمعرفة الخيارات التي تم إصلاحها تلقائيًا.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "الامتثال" على "PdfCompliance.PdfA1b" لتتوافق مع معيار "PDF/A-1b"،
// والذي يهدف إلى الحفاظ على المظهر المرئي للمستند حيث يقوم Aspose.Words بتحويله إلى PDF.
// اضبط خاصية "الامتثال" على "PdfCompliance.Pdf17" لتتوافق مع المعيار "1.7".
// اضبط خاصية "الامتثال" على "PdfCompliance.PdfA1a" لتتوافق مع معيار "PDF/A-1a"،
// والذي يتوافق مع "PDF/A-1b" بالإضافة إلى الحفاظ على بنية المستند للوثيقة الأصلية.
// اضبط خاصية "الامتثال" على "PdfCompliance.PdfUa1" لتتوافق مع معيار "PDF/UA-1" (ISO 14289-1)،
// والذي يهدف إلى تحديد المستندات الإلكترونية الممثلة في ملف PDF والتي تسمح بالوصول إلى الملف.
// اضبط خاصية "الامتثال" على "PdfCompliance.Pdf20" لتتوافق مع معيار "PDF 2.0" (ISO 32000-2).
// اضبط خاصية "الامتثال" على "PdfCompliance.PdfA4" لتتوافق مع معيار "PDF/A-4" (ISO 19004:2020)،
// الذي يحافظ على المظهر المرئي الثابت للوثيقة بمرور الوقت.
// يساعد هذا في جعل المستندات قابلة للبحث، ولكنه قد يزيد بشكل كبير من حجم المستندات الكبيرة بالفعل.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
