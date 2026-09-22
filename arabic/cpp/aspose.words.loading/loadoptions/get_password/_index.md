---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_Password"
linktitle: "get_Password"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_Password. يحصل على أو يحدد كلمة المرور لفتح مستند مشفر. يمكن أن تكون null أو سلسلة فارغة. القيمة الافتراضية هي null في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


يحصل أو يعيّن كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## ملاحظات


تحتاج إلى معرفة كلمة المرور لفتح مستند مشفر. إذا لم يكن المستند مشفرًا، اضبط هذا على **null** أو سلسلة فارغة.

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
