---
title: "Aspose::Words::DigitalSignatures::SignOptions sınıfı"
linktitle: "SignOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::SignOptions sınıfı. Belge imzalama için seçenekleri belirtmeye olanak tanır. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class


Belge imzalama için seçenekleri belirtmeye izin verir. Daha fazla bilgi için, [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) dokümantasyon makalesini ziyaret edin.

```cpp
class SignOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_ApplicationVersion](./get_applicationversion/)() const | Dijital imza için uygulama sürümünü alır veya ayarlar. Varsayılan değer "12.0". |
| [get_ColorDepth](./get_colordepth/)() const | Dijital imza için renk derinliğini alır veya ayarlar. Varsayılan değer 32. |
| [get_Comments](./get_comments/)() const | Dijital imza üzerindeki yorumları belirtir. Varsayılan değer **empty string**. |
| [get_DecryptionPassword](./get_decryptionpassword/)() const | Kaynak belgeyi çözmek için şifre. Varsayılan değer **empty string**. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Dijital imza için yatay çözünürlüğü alır veya ayarlar. Varsayılan değer 1920. |
| [get_OfficeVersion](./get_officeversion/)() const | Dijital imza için Office sürümünü alır veya ayarlar. Varsayılan değer "12.0". |
| [get_ProviderId](./get_providerid/)() const | İmza sağlayıcısının sınıf kimliğini belirtir. Varsayılan değer **Empty (all zeroes) Guid**. |
| [get_SignatureLineId](./get_signaturelineid/)() const | İmza satırı tanımlayıcısı. Varsayılan değer **Empty (all zeroes) Guid**. |
| [get_SignatureLineImage](./get_signaturelineimage/)() const | İlgili [SignatureLine](../../aspose.words.drawing/signatureline/) içinde gösterilecek görüntü. Varsayılan değer **null**. |
| [get_SignTime](./get_signtime/)() const | İmza tarihi. Varsayılan değer **current time** (**Now**) |
| [get_VerticalResolution](./get_verticalresolution/)() const | Dijital imza için dikey çözünürlüğü alır veya ayarlar. Varsayılan değer 1200. |
| [get_WindowsVersion](./get_windowsversion/)() const | Dijital imza için Windows sürümünü alır veya ayarlar. Varsayılan değer "6.1". |
| [get_XmlDsigLevel](./get_xmldsiglevel/)() const | XML-DSig standardına dayalı bir dijital imzanın seviyesini belirtir. Varsayılan değer [XmlDSig](../xmldsiglevel/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ApplicationVersion](./set_applicationversion/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_ApplicationVersion](./get_applicationversion/). |
| [set_ColorDepth](./set_colordepth/)(int32_t) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_ColorDepth](./get_colordepth/). |
| [set_Comments](./set_comments/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_Comments](./get_comments/). |
| [set_DecryptionPassword](./set_decryptionpassword/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword](./get_decryptionpassword/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(int32_t) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_OfficeVersion](./set_officeversion/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_OfficeVersion](./get_officeversion/). |
| [set_ProviderId](./set_providerid/)(System::Guid) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId](./get_providerid/). |
| [set_SignatureLineId](./set_signaturelineid/)(System::Guid) | İmza satırı tanımlayıcısı. Varsayılan değer **Empty (all zeroes) Guid**. |
| [set_SignatureLineImage](./set_signaturelineimage/)(const System::ArrayPtr\<uint8_t\>\&) | İlgili [SignatureLine](../../aspose.words.drawing/signatureline/) içinde gösterilecek görüntü. Varsayılan değer **null**. |
| [set_SignTime](./set_signtime/)(System::DateTime) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_SignTime](./get_signtime/). |
| [set_VerticalResolution](./set_verticalresolution/)(int32_t) | Ayarlayıcı: [Aspose::Words::DigitalSignatures::SignOptions::get_VerticalResolution](./get_verticalresolution/). |
| [set_WindowsVersion](./set_windowsversion/)(const System::String\&) | Ayarlayıcı [Aspose::Words::DigitalSignatures::SignOptions::get_WindowsVersion](./get_windowsversion/). |
| [set_XmlDsigLevel](./set_xmldsiglevel/)(Aspose::Words::DigitalSignatures::XmlDsigLevel) | Ayarlayıcı [Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel](./get_xmldsiglevel/). |
| [SignOptions](./signoptions/)() |  |
| static [Type](./type/)() |  |

## Örnekler



Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.
```cpp
// Özel anahtar içermesi gereken bir PKCS#12 deposundan X.509 sertifikası oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Yerel dosya sisteminden bir dosya akışı aracılığıyla imzasız bir belge alın,
// daha sonra çıktı dosya akışının dosya adıyla belirlenen imzalı bir kopyasını oluşturun.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
