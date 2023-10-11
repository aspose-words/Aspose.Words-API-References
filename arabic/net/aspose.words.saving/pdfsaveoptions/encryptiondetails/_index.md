---
title: PdfSaveOptions.EncryptionDetails
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. الحصول على أو تعيين تفاصيل تشفير مستند PDF الناتج.
type: docs
weight: 130
url: /ar/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

الحصول على أو تعيين تفاصيل تشفير مستند PDF الناتج.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

### ملاحظات

القيمة الافتراضية هي`باطل` ولن يتم تشفير مستند الإخراج. عندما يتم تعيين هذه الخاصية إلى صالحة[`PdfEncryptionDetails`](../../pdfencryptiondetails/) object, ثم سيتم تشفير مستند PDF الناتج.

يتم استخدام خوارزمية التشفير AES-128 عند الحفظ إلى التوافق المستند إلى PDF 1.7 (بما في ذلك PDF/UA-1). يتم استخدام خوارزمية التشفير AES-256 عند الحفظ إلى التوافق المستند إلى PDF 2.0.

التشفير محظور بموجب التوافق مع PDF/A. سيتم تجاهل هذا الخيار عند الحفظ إلى PDF/A.

ContentCopyForAccessibility مطلوب إذن من خلال الامتثال لـ PDF/UA إذا كان مستند الإخراج مشفرًا. سيتم استخدام هذا الإذن تلقائيًا عند الحفظ إلى PDF/UA.

ContentCopyForAccessibility تم إهمال الإذن بتنسيق PDF 2.0. سيتم تجاهل هذا الإذن عند الحفظ في PDF 2.0.

### أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// توسيع الأذونات للسماح بتحرير التعليقات التوضيحية.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند، سنحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


