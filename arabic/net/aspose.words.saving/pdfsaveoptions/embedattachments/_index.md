---
title: PdfSaveOptions.EmbedAttachments
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم تضمين المرفقات في مستند PDF أم لا.
type: docs
weight: 110
url: /ar/net/aspose.words.saving/pdfsaveoptions/embedattachments/
---
## PdfSaveOptions.EmbedAttachments property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم تضمين المرفقات في مستند PDF أم لا.

```csharp
public bool EmbedAttachments { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`خطأ شنيع`ولا يتم تضمين المرفقات.

عندما تكون القيمة`حقيقي` يتم تضمين المرفقات في وثيقة PDF.

تضمين المرفقات غير مدعوم عند الحفظ بتنسيق PDF/A وPDF/UA. `خطأ شنيع` سيتم استخدام القيمة تلقائيًا.

تضمين المرفقات غير مدعوم عند تمكين التشفير.`خطأ شنيع` سيتم استخدام value تلقائيًا.

### أمثلة

يوضح كيفية إضافة مرفقات مضمنة إلى مستند PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

PdfSaveOptions options = new PdfSaveOptions();
options.EmbedAttachments = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.PdfEmbedAttachments.pdf", options);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


