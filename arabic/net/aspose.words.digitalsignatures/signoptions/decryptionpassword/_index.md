---
title: SignOptions.DecryptionPassword
linktitle: DecryptionPassword
articleTitle: DecryptionPassword
second_title: Aspose.Words لـ .NET
description: افتح مستنداتك بسهولة مع ميزة DecryptionPassword من SignOptions. فك تشفير ملفات المصدر بأمان وسهولة؛ الإعداد الافتراضي هو سلسلة فارغة.
type: docs
weight: 30
url: /ar/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي**سلسلة فارغة** (Empty ).

```csharp
public string DecryptionPassword { get; set; }
```

## ملاحظات

إذا تم تشفير مستند OOXML، فيجب عليك توفير كلمة مرور فك التشفير لفك تشفير مستند المصدر قبل توقيعه. لا يلزم هذا بالنسبة للمستندات بتنسيق DOC الثنائي.

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

* class [SignOptions](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* المجسم [Aspose.Words](../../../)
