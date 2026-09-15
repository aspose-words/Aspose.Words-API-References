---
title: "Aspose::Words::DigitalSignatures::CertificateHolder class"
linktitle: "CertificateHolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder class. يمثل حاملاً لكائن X509Certificate2. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


يمثل حاملاً لنسخة **X509Certificate2**. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | ينشئ كائن [CertificateHolder](./) باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | ينشئ كائن [CertificateHolder](./) باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](./create/)(const System::String\&, const System::String\&) | ينشئ كائن [CertificateHolder](./) باستخدام مسار إلى مخزن PKCS12 وكلمة المرور الخاصة به. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | ينشئ كائن [CertificateHolder](./) باستخدام مسار إلى مخزن PKCS12، وكلمة المرور الخاصة به، والاسم المستعار الذي يُستخدم للعثور على المفتاح الخاص والشهادة. |
| [get_Certificate](./get_certificate/)() | يرجع نسخة من **X509Certificate2** التي تحتفظ بالمفاتيح الخاصة والعامة وسلسلة الشهادات. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

## أمثلة



يوضح كيفية توقيع المستندات رقمياً.
```cpp
// إنشاء شهادة X.509 من مخزن PKCS#12، والذي يجب أن يحتوي على مفتاح خاص.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// إنشاء تعليق وتاريخ سيتم تطبيقهما مع توقيعنا الرقمي الجديد.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// أخذ مستند غير موقع من نظام الملفات المحلي عبر تدفق ملف،
// ثم إنشاء نسخة موقعة منه يتم تحديدها بواسطة اسم ملف تدفق الإخراج.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
