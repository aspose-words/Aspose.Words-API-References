---
title: PdfEncryptionDetails.OwnerPassword
linktitle: OwnerPassword
articleTitle: OwnerPassword
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُؤمّن خاصية OwnerPassword ملفات PDF المُشفّرة، مما يضمن الوصول المُصرّح به فقط. احمِ مستنداتك بكل سهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

يحدد كلمة مرور المالك لمستند PDF المشفر.

```csharp
public string OwnerPassword { get; set; }
```

## ملاحظات

تتيح كلمة مرور المالك للمستخدم فتح مستند PDF مشفر دون أي قيود وصول المحددة في[`Permissions`](../permissions/).

لا يمكن أن تكون كلمة مرور المالك هي نفسها كلمة مرور المستخدم.

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

* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
