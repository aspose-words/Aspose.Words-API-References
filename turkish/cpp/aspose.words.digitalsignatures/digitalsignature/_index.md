---
title: "Aspose::Words::DigitalSignatures::DigitalSignature class"
linktitle: "DigitalSignature"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignature sınıfı. Bir belgede dijital imzayı ve doğrulama sonucunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class


Bir belgede dijital imzayı ve doğrulama sonucunu temsil eder. Daha fazla bilgi için, [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) dokümantasyon makalesini ziyaret edin.

```cpp
class DigitalSignature : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() | Dijital imza için uygulama sürümünü alır. |
| [get_CertificateHolder](./get_certificateholder/)() const | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [get_ColorDepth](./get_colordepth/)() | Dijital imza için renk derinliğini alır. |
| [get_Comments](./get_comments/)() | İmza amacı yorumunu alır. |
| [get_HorizontalResolution](./get_horizontalresolution/)() | Dijital imza için yatay çözünürlüğü alır. |
| [get_IssuerName](./get_issuername/)() | Sertifika verenin konu ayırt edici adını döndürür. |
| [get_IsValid](./get_isvalid/)() const | Bu dijital imza geçerli ve belge değiştirilmemişse **true** döndürür. |
| [get_OfficeVersion](./get_officeversion/)() | Dijital imza için Office sürümünü alır. |
| [get_SignatureType](./get_signaturetype/)() const | Dijital imzanın türünü alır. |
| [get_SignatureValue](./get_signaturevalue/)() const | İmza değerini temsil eden bir bayt dizisini alır. |
| [get_SignTime](./get_signtime/)() const | Belgenin imzalanma zamanını alır. |
| [get_SubjectName](./get_subjectname/)() | Belgeyi imzalamak için kullanılan sertifikanın konu ayırt edici adını döndürür. |
| [get_VerticalResolution](./get_verticalresolution/)() | Dijital imza için dikey çözünürlüğü alır. |
| [get_WindowsVersion](./get_windowsversion/)() | Dijital imza için Windows sürümünü alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür. |
| static [Type](./type/)() |  |

## Örnekler



Bir belgede bulunan her imzanın doğrulanması ve bilgilerinin gösterilmesi nasıl yapılır gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
