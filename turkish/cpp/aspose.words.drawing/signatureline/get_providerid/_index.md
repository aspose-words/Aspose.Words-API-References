---
title: "Aspose::Words::Drawing::SignatureLine::get_ProviderId metodu"
linktitle: "get_ProviderId"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::SignatureLine::get_ProviderId metodu. Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer C++'ta \"{00000000-0000-0000-0000-000000000000}\"'dır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.drawing/signatureline/get_providerid/
---
## SignatureLine::get_ProviderId method


Bu imza satırı için imza sağlayıcı tanımlayıcısını alır veya ayarlar. Varsayılan değer "{00000000-0000-0000-0000-000000000000}".

```cpp
System::Guid Aspose::Words::Drawing::SignatureLine::get_ProviderId()
```

## Açıklamalar


Kriptografik hizmet sağlayıcısı (CSP), kimlik doğrulama, kodlama ve şifreleme için kriptografi algoritmalarını gerçekte yürüten bağımsız bir yazılım modülüdür. MS Office, varsayılan imza sağlayıcısı için {00000000-0000-0000-0000-000000000000} değerini ayırır.

Ek olarak kurulan sağlayıcının GUID'i, sağlayıcıyla birlikte gelen belgelerden alınmalıdır.

Ayrıca, yüklü tüm kriptografik sağlayıcılar Windows kayıt defterinde listelenir. Aşağıdaki yolda bulunabilir: HKLM\\SOFTWARE\\**Microsoft**\\Cryptography\\Defaults\\Provider. \"CP Service UUID\" adlı bir anahtar vardır ve bu, imza sağlayıcısının GUID'ine karşılık gelir.

## Örnekler



Kişisel bir sertifika ve imza satırıyla bir belgeyi nasıl imzalayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto signatureLineOptions = System::MakeObject<Aspose::Words::SignatureLineOptions>();
signatureLineOptions->set_Signer(u"vderyushev");
signatureLineOptions->set_SignerTitle(u"QA");
signatureLineOptions->set_Email(u"vderyushev@aspose.com");
signatureLineOptions->set_ShowDate(true);
signatureLineOptions->set_DefaultInstructions(false);
signatureLineOptions->set_Instructions(u"Please sign here.");
signatureLineOptions->set_AllowComments(true);

System::SharedPtr<Aspose::Words::Drawing::SignatureLine> signatureLine = builder->InsertSignatureLine(signatureLineOptions)->get_SignatureLine();
signatureLine->set_ProviderId(System::Guid::Parse(u"CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

ASSERT_FALSE(signatureLine->get_IsSigned());
ASSERT_FALSE(signatureLine->get_IsValid());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignatureLineId(signatureLine->get_Id());
signOptions->set_ProviderId(signatureLine->get_ProviderId());
signOptions->set_Comments(u"Document was signed by vderyushev");
signOptions->set_SignTime(System::DateTime::get_Now());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.docx", get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// Kaydedilmiş belgemizi yeniden açın ve "IsSigned" ve "IsValid" özelliklerinin her ikisinin de "true" olduğunu doğrulayın,
// bu, imza satırının bir imza içerdiğini gösterir.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Ayrıca Bakınız

* Class [SignatureLine](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
