---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: LoadOptions Password ملكية. الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن يكونباطل أو سلسلة فارغة. الافتراضي هوباطل  في C#.
type: docs
weight: 110
url: /ar/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

الحصول على كلمة المرور أو تعيينها لفتح مستند مشفر. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` .

```csharp
public string Password { get; set; }
```

## ملاحظات

تحتاج إلى معرفة كلمة المرور لفتح مستند مشفر. إذا لم يكن المستند مشفرًا، فاضبط هذا على`باطل` أو سلسلة فارغة.

## أمثلة

يوضح كيفية توقيع ملف المستند المشفر.

```csharp
// أنشئ شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// أنشئ تعليقًا وتاريخًا وكلمة مرور لفك التشفير والتي سيتم تطبيقها مع توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// قم بتعيين اسم ملف النظام المحلي لمستند الإدخال غير الموقع، واسم ملف الإخراج لنسخته الجديدة الموقعة رقميًا.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
