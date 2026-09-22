---
title: "Aspose::Words::DigitalSignatures::CertificateHolder::Create yöntemi"
linktitle: "Create"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::CertificateHolder::Create yöntemi. C++'da PKCS12 deposunun bayt dizisini ve şifresini kullanarak CertificateHolder nesnesi oluşturur."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.digitalsignatures/certificateholder/create/
---
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) method


PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](../) nesnesi oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::SharedPtr<System::Security::SecureString> &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | X.509 sertifikasından veri içeren bir bayt dizisi. |
| password | const System::SharedPtr\<System::Security::SecureString\>\& | X.509 sertifika verilerine erişmek için gerekli şifre. |

### ReturnValue

Bir [CertificateHolder](../) örneği

## Ayrıca Bakınız

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) method


PKCS12 deposunun bayt dizisini ve şifresini kullanarak [CertificateHolder](../) nesnesi oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::ArrayPtr<uint8_t> &certBytes, const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| certBytes | const System::ArrayPtr\<uint8_t\>\& | X.509 sertifikasından veri içeren bir bayt dizisi. |
| password | const System::String\& | X.509 sertifika verilerine erişmek için gerekli şifre. |

### ReturnValue

Bir [CertificateHolder](../) örneği

## Ayrıca Bakınız

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&) method


PKCS12 deposunun yolunu ve şifresini kullanarak bir [CertificateHolder](../) nesnesi oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Bir sertifika dosyasının adı. |
| password | const System::String\& | X.509 sertifika verilerine erişmek için gerekli şifre. |

### ReturnValue

Bir [CertificateHolder](../) örneği

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

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## CertificateHolder::Create(const System::String\&, const System::String\&, const System::String\&) method


PKCS12 deposunun yolu, şifresi ve özel anahtar ile sertifikanın bulunacağı takma adı kullanarak bir [CertificateHolder](../) nesnesi oluşturur.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> Aspose::Words::DigitalSignatures::CertificateHolder::Create(const System::String &fileName, const System::String &password, const System::String &alias)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Bir sertifika dosyasının adı. |
| password | const System::String\& | X.509 sertifika verilerine erişmek için gerekli şifre. |
| takma ad | const System::String\& | Bir sertifika ve onun özel anahtarı için ilişkili takma ad |

### ReturnValue

Bir [CertificateHolder](../) örneği

## Ayrıca Bakınız

* Class [CertificateHolder](../)
* Class [CertificateHolder](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
