---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_SignTime yöntemi"
linktitle: "get_SignTime"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_SignTime yöntemi. İmza tarihi. Varsayılan değer C++'ta geçerli zaman (Now) dır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.digitalsignatures/signoptions/get_signtime/
---
## SignOptions::get_SignTime method


İmza tarihi. Varsayılan değer **current time** (**Now**)

```cpp
System::DateTime Aspose::Words::DigitalSignatures::SignOptions::get_SignTime() const
```


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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
