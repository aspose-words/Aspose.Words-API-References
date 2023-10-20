---
title: PdfEncryptionDetails
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words لـ .NET
description: PdfEncryptionDetails البناء. تهيئة مثيل لهذه الفئة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pdfencryptiondetails/pdfencryptiondetails/
---
## PdfEncryptionDetails(*string, string*) {#constructor}

تهيئة مثيل لهذه الفئة.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword)
```

### أنظر أيضا

* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## PdfEncryptionDetails(*string, string, [PdfPermissions](../../pdfpermissions/)*) {#constructor_1}

تهيئة مثيل لهذه الفئة.

```csharp
public PdfEncryptionDetails(string userPassword, string ownerPassword, PdfPermissions permissions)
```

## أمثلة

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

* enum [PdfPermissions](../../pdfpermissions/)
* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
