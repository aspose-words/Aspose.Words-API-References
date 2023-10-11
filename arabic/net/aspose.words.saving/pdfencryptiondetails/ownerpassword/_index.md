---
title: PdfEncryptionDetails.OwnerPassword
second_title: Aspose.Words لمراجع .NET API
description: PdfEncryptionDetails ملكية. يحدد كلمة مرور المالك لمستند PDF المشفر.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pdfencryptiondetails/ownerpassword/
---
## PdfEncryptionDetails.OwnerPassword property

يحدد كلمة مرور المالك لمستند PDF المشفر.

```csharp
public string OwnerPassword { get; set; }
```

### ملاحظات

تسمح كلمة مرور المالك للمستخدم بفتح مستند PDF مشفر دون أي قيود وصول محددة في[`Permissions`](../permissions/).

لا يمكن أن تكون كلمة مرور المالك هي نفس كلمة مرور المستخدم.

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

* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfencryptiondetails/)
* المجسم [Aspose.Words](../../../)


