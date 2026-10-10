---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create طريقة"
linktitle: "Create"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create طريقة. ينشئ كائن CertificateHolder باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة مروره في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


ينشئ كائن [CertificateHolder](../) باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة مروره.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة بايت تحتوي على بيانات من شهادة X.509. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### ReturnValue

مثال من [CertificateHolder](../)

## انظر أيضًا

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


ينشئ كائن [CertificateHolder](../) باستخدام مصفوفة بايت من مخزن PKCS12 وكلمة مروره.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | مصفوفة بايت تحتوي على بيانات من شهادة X.509. |
| password | const System::String\& | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### ReturnValue

مثال من [CertificateHolder](../)

## انظر أيضًا

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


ينشئ كائن [CertificateHolder](../) باستخدام مسار مخزن PKCS12 وكلمة مروره.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف الشهادة. |
| password | const System::String\& | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |

### ReturnValue

مثال من [CertificateHolder](../)

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

## انظر أيضًا

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


ينشئ كائن [CertificateHolder](../) باستخدام مسار مخزن PKCS12، وكلمة مروره، والاسم المستعار الذي سيتم من خلاله العثور على المفتاح الخاص والشهادة.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف الشهادة. |
| password | const System::String\& | كلمة المرور المطلوبة للوصول إلى بيانات شهادة X.509. |
| الاسم المستعار | const System::String\& | الاسم المستعار المرتبط بشهادة ومفتاحها الخاص |

### ReturnValue

مثال من [CertificateHolder](../)

## انظر أيضًا

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
