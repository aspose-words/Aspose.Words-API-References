---
title: "Aspose::Words::DigitalSignatures::DigitalSignature class"
linktitle: "DigitalSignature"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignature class. يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


يمثل توقيعًا رقميًا على مستند ونتيجة التحقق منه. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignature : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | يحصل على إصدار التطبيق للتوقيع الرقمي. |
| [get_CertificateHolder](./get_certificateholder/)() const | يعيد كائن حامل الشهادة الذي يحتوي على الشهادة المستخدمة لتوقيع المستند. |
| [get_ColorDepth](./get_colordepth/)() | يحصل على عمق اللون للتوقيع الرقمي. |
| [get_Comments](./get_comments/)() | يحصل على تعليق هدف التوقيع. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | يحصل على الدقة الأفقية للتوقيع الرقمي. |
| [get_IssuerName](./get_issuername/)() | يعيد الاسم المميز للموضوع للجهة المصدرة للشهادة. |
| [get_IsValid](./get_isvalid/)() const | يعيد **true** إذا كان هذا التوقيع الرقمي صالحًا ولم يتم العبث بالمستند. |
| [get_OfficeVersion](./get_officeversion/)() | يحصل على إصدار Office للتوقيع الرقمي. |
| [get_SignatureType](./get_signaturetype/)() const | يحصل على نوع التوقيع الرقمي. |
| [get_SignatureValue](./get_signaturevalue/)() const | يحصل على مصفوفة من البايتات تمثل قيمة التوقيع. |
| [get_SignTime](./get_signtime/)() const | يحصل على وقت توقيع المستند. |
| [get_SubjectName](./get_subjectname/)() | يعيد الاسم المميز للموضوع للشهادة التي تم استخدامها لتوقيع المستند. |
| [get_VerticalResolution](./get_verticalresolution/)() | يحصل على الدقة العمودية للتوقيع الرقمي. |
| [get_WindowsVersion](./get_windowsversion/)() | يحصل على إصدار Windows للتوقيع الرقمي. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن. |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية التحقق من صحة وعرض معلومات كل توقيع في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```

## انظر أيضًا

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
