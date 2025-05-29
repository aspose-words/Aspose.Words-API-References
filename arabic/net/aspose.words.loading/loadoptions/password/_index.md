---
title: LoadOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words لـ .NET
description: أدر مستنداتك المشفرة بسهولة باستخدام خاصية LoadOptions Password. اضبط كلمة مرورك أو استردها بأمان لضمان وصول سلس.
type: docs
weight: 110
url: /ar/net/aspose.words.loading/loadoptions/password/
---
## LoadOptions.Password property

يحصل على كلمة المرور لفتح مستند مشفر أو يعينها. يمكن أن يكون`باطل` أو سلسلة فارغة. الافتراضي هو`باطل` .

```csharp
public string Password { get; set; }
```

## ملاحظات

يجب أن تعرف كلمة المرور لفتح مستند مشفّر. إذا لم يكن المستند مشفّرًا، فاضبطه على`باطل` أو سلسلة فارغة.

## أمثلة

يوضح كيفية توقيع ملف مستند مشفر.

```csharp
// قم بإنشاء شهادة X.509 من متجر PKCS#12، والتي يجب أن تحتوي على مفتاح خاص.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// قم بإنشاء تعليق وتاريخ وكلمة مرور فك التشفير والتي سيتم تطبيقها باستخدام توقيعنا الرقمي الجديد.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// تعيين اسم ملف النظام المحلي للمستند الإدخالي غير الموقع، واسم ملف الإخراج للنسخة الجديدة الموقعة رقميًا.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### أنظر أيضا

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
