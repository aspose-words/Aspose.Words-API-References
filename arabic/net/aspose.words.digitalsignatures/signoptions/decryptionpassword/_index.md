---
title: SignOptions.DecryptionPassword
second_title: Aspose.Words لمراجع .NET API
description: SignOptions ملكية. كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي سلسلة فارغة Empty.
type: docs
weight: 30
url: /ar/net/aspose.words.digitalsignatures/signoptions/decryptionpassword/
---
## SignOptions.DecryptionPassword property

كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي **سلسلة فارغة** (Empty).

```csharp
public string DecryptionPassword { get; set; }
```

### ملاحظات

إذا تم تشفير مستند OOXML، فيجب عليك توفير كلمة مرور فك التشفير لفك تشفير المستند المصدر قبل أن يتم توقيعه. هذا غير مطلوب للمستندات بتنسيق DOC الثنائي.

### أمثلة

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

* class [SignOptions](../)
* مساحة الاسم [Aspose.Words.DigitalSignatures](../../signoptions/)
* المجسم [Aspose.Words](../../../)


