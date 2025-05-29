---
title: PdfSaveOptions.AttachmentsEmbeddingMode
linktitle: AttachmentsEmbeddingMode
articleTitle: AttachmentsEmbeddingMode
second_title: Aspose.Words لـ .NET
description: خصّص طريقة تضمين المرفقات في ملفات PDF باستخدام PdfSaveOptions. اضمن تكاملاً سلساً ومشاركةً مُحسّنة للمستندات.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/
---
## PdfSaveOptions.AttachmentsEmbeddingMode property

يحصل على قيمة تحدد كيفية تضمين المرفقات في مستند PDF أو يعينها.

```csharp
public PdfAttachmentsEmbeddingMode AttachmentsEmbeddingMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone والمرفقات غير مضمنة.

لا تسمح معايير PDF/A-1 وPDF/A-2 وPDF/A-4 العادية (وليس PDF/A-4f) بالملفات المضمنة. None سيتم استخدام القيمة تلقائيًا.

## أمثلة

يوضح كيفية إضافة المرفقات المضمنة إلى مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.AttachmentsEmbeddingMode = PdfAttachmentsEmbeddingMode.Annotations;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfAttachmentsEmbeddingMode](../../pdfattachmentsembeddingmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
