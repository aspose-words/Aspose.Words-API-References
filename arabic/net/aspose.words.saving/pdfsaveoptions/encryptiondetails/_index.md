---
title: PdfSaveOptions.EncryptionDetails
linktitle: EncryptionDetails
articleTitle: EncryptionDetails
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية EncryptionDetails في PdfSaveOptions لتكوين إعدادات تشفير PDF بسهولة، مما يضمن بقاء مستنداتك آمنة ومحمية.
type: docs
weight: 130
url: /ar/net/aspose.words.saving/pdfsaveoptions/encryptiondetails/
---
## PdfSaveOptions.EncryptionDetails property

يحصل على تفاصيل تشفير مستند PDF الناتج أو يعينها.

```csharp
public PdfEncryptionDetails EncryptionDetails { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`باطل` ولن يتم تشفير المستند الناتج. عندما يتم تعيين هذه الخاصية على قيمة صالحة[`PdfEncryptionDetails`](../../pdfencryptiondetails/)الكائن، ثم سيتم تشفير مستند PDF الناتج.

يتم استخدام خوارزمية التشفير AES-128 عند الحفظ وفقًا للتوافق مع PDF 1.7 (بما في ذلك PDF/UA-1). يتم استخدام خوارزمية التشفير AES-256 عند الحفظ وفقًا للتوافق مع PDF 2.0.

التشفير محظور بموجب توافق PDF/A. سيتم تجاهل هذا الخيار عند الحفظ بتنسيق PDF/A.

ContentCopyForAccessibility يتطلب PDF/UA compliance إذنًا إذا كان المستند الناتج مشفّرًا. سيتم استخدام هذا الإذن تلقائيًا عند الحفظ بتنسيق PDF/UA.

ContentCopyForAccessibility تم إلغاء الإذن في تنسيق PDF 2.0. سيتم تجاهل هذا الإذن عند الحفظ في PDF 2.0.

## أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// تمديد الأذونات للسماح بتحرير التعليقات التوضيحية.
PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty, PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly);

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند، سوف نحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfEncryptionDetails](../../pdfencryptiondetails/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
