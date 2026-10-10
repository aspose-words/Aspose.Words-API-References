---
title: "Aspose::Words::DigitalSignatures::CertificateHolder class"
linktitle: "CertificateHolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::CertificateHolder class. X509Certificate2 örneğinin tutucusunu temsil eder. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Bir **X509Certificate2** örneği tutucusunu temsil eder. Daha fazla bilgi için, [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) dokümantasyon makalesini ziyaret edin.

```cpp
class CertificateHolder : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](./) nesnesi oluşturur. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](./) nesnesi oluşturur. |
| static [Create](./create/)(const System::String\&, const System::String\&) | PKCS12 deposunun yolunu ve şifresini kullanarak [CertificateHolder](./) nesnesi oluşturur. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | PKCS12 deposunun yolunu, şifresini ve özel anahtar ile sertifikanın bulunacağı takma adı kullanarak [CertificateHolder](./) nesnesi oluşturur. |
| [get_Certificate](./get_certificate/)() | Özel ve genel anahtarları ve sertifika zincirini tutan **X509Certificate2** örneğini döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


Şifreli belge dosyasını imzalamanın nasıl yapılacağını gösterir.
```cpp
// Özel anahtar içermesi gereken bir PKCS#12 deposundan X.509 sertifikası oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme parolası oluşturun.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// İmzalanmamış giriş belgesi için yerel sistem dosya adını ayarlayın ve yeni dijital olarak imzalanmış kopyası için bir çıktı dosya adı belirleyin.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
