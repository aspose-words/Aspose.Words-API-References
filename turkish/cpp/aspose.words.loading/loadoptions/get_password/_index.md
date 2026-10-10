---
title: "Aspose::Words::Loading::LoadOptions::get_Password yöntemi"
linktitle: "get_Password"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_Password yöntemi. Şifreli bir belgeyi açmak için şifreyi alır veya ayarlar. Null veya boş dize olabilir. Varsayılan değer C++'da null'dur."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Şifreli bir belgeyi açmak için parolayı alır veya ayarlar. **null** veya boş dize olabilir. Varsayılan **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Açıklamalar


Şifreli bir belgeyi açmak için şifreyi bilmeniz gerekir. Belge şifreli değilse, bunu **null** veya boş dize olarak ayarlayın.

## Örnekler



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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
