---
title: PdfEncryptionDetails Class
linktitle: PdfEncryptionDetails
articleTitle: PdfEncryptionDetails
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.PdfEncryptionDetails فصل. يحتوي على تفاصيل التشفير وأذونات الوصول لمستند PDF في C#.
type: docs
weight: 5460
url: /ar/net/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class

يحتوي على تفاصيل التشفير وأذونات الوصول لمستند PDF.

لمعرفة المزيد، قم بزيارة[حماية أو تشفير مستند](https://docs.aspose.com/words/net/protect-or-encrypt-a-document/) مقالة توثيقية.

```csharp
public class PdfEncryptionDetails
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor)(*string, string*) | تهيئة مثيل لهذه الفئة. |
| [PdfEncryptionDetails](pdfencryptiondetails/#constructor_1)(*string, string, [PdfPermissions](../pdfpermissions/)*) | تهيئة مثيل لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [OwnerPassword](../../aspose.words.saving/pdfencryptiondetails/ownerpassword/) { get; set; } | يحدد كلمة مرور المالك لمستند PDF المشفر. |
| [Permissions](../../aspose.words.saving/pdfencryptiondetails/permissions/) { get; set; } | يحدد العمليات المسموح بها للمستخدم على مستند PDF مشفر. القيمة الافتراضية هيDisallowAll . |
| [UserPassword](../../aspose.words.saving/pdfencryptiondetails/userpassword/) { get; set; } | يحدد كلمة مرور المستخدم المطلوبة لفتح مستند PDF المشفر. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
