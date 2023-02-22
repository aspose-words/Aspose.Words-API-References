---
title: PdfEncryptionDetails.UserPassword
second_title: Aspose.Words لمراجع .NET API
description: PdfEncryptionDetails ملكية. يحدد كلمة مرور المستخدم المطلوبة لفتح مستند PDF المشفر.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

يحدد كلمة مرور المستخدم المطلوبة لفتح مستند PDF المشفر.

```csharp
public string UserPassword { get; set; }
```

### ملاحظات

ستكون كلمة مرور المستخدم مطلوبة لفتح مستند PDF مشفر لعرضه. الأذونات المحددة في [`Permissions`](../permissions/) سيتم فرضه بواسطة برنامج القارئ.

يمكن أن تكون كلمة مرور المستخدم فارغة أو سلسلة فارغة ، وفي هذه الحالة لن تكون كلمة المرور مطلوبة من المستخدم عند فتح مستند PDF. لا يمكن أن تكون كلمة مرور المستخدم هي نفسها كلمة مرور المالك.

### أمثلة

يوضح كيفية تعيين الأذونات على مستند PDF محفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

PdfEncryptionDetails encryptionDetails =
    new PdfEncryptionDetails("password", string.Empty);

// ابدأ برفض جميع الأذونات.
encryptionDetails.Permissions = PdfPermissions.DisallowAll;

// تمديد الأذونات للسماح بتحرير التعليقات التوضيحية.
encryptionDetails.Permissions = PdfPermissions.ModifyAnnotations | PdfPermissions.DocumentAssembly;

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// تمكين التشفير عبر خاصية "EncryptionDetails".
saveOptions.EncryptionDetails = encryptionDetails;

// عندما نفتح هذا المستند ، سنحتاج إلى توفير كلمة المرور قبل الوصول إلى محتوياته.
doc.Save(ArtifactsDir + "PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfEncryptionDetails](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfencryptiondetails/)
* المجسم [Aspose.Words](../../../)


