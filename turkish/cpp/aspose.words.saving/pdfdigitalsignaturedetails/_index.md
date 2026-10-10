---
title: "Aspose::Words::Saving::PdfDigitalSignatureDetails sınıfı"
linktitle: "PdfDigitalSignatureDetails"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfDigitalSignatureDetails sınıfı. C++'da bir PDF belgesini dijital imza ile imzalamak için gerekli ayrıntıları içerir."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Bir PDF belgesini dijital imza ile imzalama ayrıntılarını içerir.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Karma algoritmasını alır. |
| [get_Location](./get_location/)() const | İmzanın konumunu alır. |
| [get_Reason](./get_reason/)() const | İmzanın nedenini alır. |
| [get_SignatureDate](./get_signaturedate/)() const | İmzanın tarihini alır veya ayarlar. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Dijital imza zaman damgası ayarlarını alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Bu sınıfın bir örneğini başlatır. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Bu sınıfın bir örneğini başlatır. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Belgeyi imzalamak için kullanılan sertifikayı içeren sertifika sahibi nesnesini döndürür. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Hash algoritmasını ayarlar. |
| [set_Location](./set_location/)(const System::String\&) | İmzanın konumunu ayarlar. |
| [set_Reason](./set_reason/)(const System::String\&) | İmza nedeni ayarlar. |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/) için ayarlayıcı. |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Şu anda PDF belgelerini dijital olarak imzalamak yalnızca .NET 3.5 veya üzeri sürümlerde kullanılabilir.

Aspose.Words tarafından oluşturulan bir PDF belgesini dijital olarak imzalamak için, [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) özelliğini geçerli bir [PdfDigitalSignatureDetails](./) nesnesine ayarlayın ve ardından belgeyi PDF formatında kaydederken [PdfSaveOptions](../pdfsaveoptions/) parametresini [Save()](../) metoduna aktarın.

Aspose.Words, tüm PDF belgesi üzerinde bir PKCS#7 imzası oluşturur ve dijital imza oluştururken \"Adobe.PPKMS\" filtresi ve \"adbe.pkcs7.sha1\" alt filtresini kullanır.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
