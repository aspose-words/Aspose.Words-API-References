---
title: PdfEncryptionDetails.UserPassword
linktitle: UserPassword
articleTitle: UserPassword
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية UserPassword على تعزيز أمان ملفات PDF من خلال طلب كلمة مرور للوصول إليها، مما يضمن بقاء مستنداتك محمية وسرية.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/pdfencryptiondetails/userpassword/
---
## PdfEncryptionDetails.UserPassword property

يحدد كلمة مرور المستخدم المطلوبة لفتح مستند PDF المشفر.

```csharp
public string UserPassword { get; set; }
```

## ملاحظات

سيُطلب إدخال كلمة مرور المستخدم لفتح مستند PDF مشفّر للعرض. الأذونات المحددة في [`Permissions`](../permissions/) سيتم تنفيذ ذلك بواسطة برنامج القارئ.

يمكن أن تكون كلمة مرور المستخدم`باطل` أو سلسلة فارغة، في هذه الحالة، لن يُطلب من المستخدم إدخال كلمة مرور عند فتح مستند PDF. لا يمكن أن تكون كلمة مرور المستخدم هي نفسها كلمة مرور المالك.

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
