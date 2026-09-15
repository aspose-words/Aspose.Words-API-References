---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments طريقة"
linktitle: "get_Comments"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments طريقة. يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.digitalsignatures/signoptions/get_comments/
---
## SignOptions::get_Comments method


يحدد التعليقات على التوقيع الرقمي. القيمة الافتراضية هي **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_Comments() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
