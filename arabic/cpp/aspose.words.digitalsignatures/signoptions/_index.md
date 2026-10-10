---
title: "فئة Aspose::Words::DigitalSignatures::SignOptions"
linktitle: "SignOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::DigitalSignatures::SignOptions. يسمح بتحديد الخيارات لتوقيع المستند. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


يسمح بتحديد خيارات توقيع المستند. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | يحصل أو يضبط إصدار التطبيق للتوقيع الرقمي. القيمة الافتراضية هي \"12.0\". |
| [get_ColorDepth](./get_colordepth/)() const | يحصل أو يضبط عمق اللون للتوقيع الرقمي. القيمة الافتراضية هي 32. |
| [get_Comments](./get_comments/)() const | يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | كلمة المرور لفك تشفير المستند المصدر. القيمة الافتراضية هي **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | يحصل أو يضبط الدقة الأفقية للتوقيع الرقمي. القيمة الافتراضية هي 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | يحصل أو يضبط إصدار Office للتوقيع الرقمي. القيمة الافتراضية هي \"12.0\". |
| [get_ProviderId](./get_providerid/)() const | يحدد معرف الفئة لمزود التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | معرف سطر التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | الصورة التي ستظهر في [SignatureLine](../../aspose.words.drawing/signatureline/) المرتبطة. القيمة الافتراضية هي **null**. |
| [get_SignTime](./get_signtime/)() const | تاريخ التوقيع. القيمة الافتراضية هي **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | يحصل أو يضبط الدقة العمودية للتوقيع الرقمي. القيمة الافتراضية هي 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | يحصل أو يضبط إصدار Windows للتوقيع الرقمي. القيمة الافتراضية هي \"6.1\". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig. القيمة الافتراضية هي [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | معرف سطر التوقيع. القيمة الافتراضية هي **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | الصورة التي ستظهر في [SignatureLine](../../aspose.words.drawing/signatureline/) المرتبطة. القيمة الافتراضية هي **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | المُعيّن لـ [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | المحدد لـ [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | المحدد لـ [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
