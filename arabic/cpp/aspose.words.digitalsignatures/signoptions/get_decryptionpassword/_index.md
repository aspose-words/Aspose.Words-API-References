---
title: "طريقة Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword"
linktitle: "get_DecryptionPassword"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword طريقة. كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


## أمثلة



يوضح كيفية توقيع ملف مستند مشفر.
```cpp
// إنشاء شهادة X.509 من مخزن PKCS#12، والذي يجب أن يحتوي على مفتاح خاص.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// إنشاء تعليق وتاريخ وكلمة مرور فك التشفير التي سيتم تطبيقها مع توقيعنا الرقمي الجديد.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// حدد اسم ملف نظام محلي للمستند غير الموقع كمدخل، واسم ملف إخراج للنسخة الموقعة رقمياً الجديدة.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## انظر أيضًا

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
