---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::SignatureLineOptions class. Eklenecek imza satırı için seçenekleri belirtmeye olanak tanır. DocumentBuilder içinde kullanılır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 61000
url: /tr/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Eklenecek imza satırı için seçenekleri belirtmeye olanak tanır. [DocumentBuilder](../documentbuilder/) içinde kullanılır. Daha fazla bilgi için [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) belge makalesini ziyaret edin.

```cpp
class SignatureLineOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | İmzalayanın İmzala iletişim kutusunda yorum ekleyebileceğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | İmzalama iletişim kutusunda varsayılan talimatların gösterildiğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **true**. |
| [get_Email](./get_email/)() const | Önerilen imzalayanın e-posta adresini alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [get_Instructions](./get_instructions/)() const | İmza satırını imzalarken imzalayana gösterilen talimatları alır veya ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [get_ShowDate](./get_showdate/)() const | İmza satırında imza tarihinin gösterildiğini belirten bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri **true**. |
| [get_Signer](./get_signer/)() const | İmza satırının önerilen imzalayanını alır. Bu özelliğin varsayılan değeri **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Önerilen imzalayanın unvanını alır. Bu özelliğin varsayılan değeri **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/) için ayarlayıcı. |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/) için ayarlayıcı. |
| [set_Email](./set_email/)(const System::String\&) | [Aspose::Words::SignatureLineOptions::get_Email](./get_email/) için ayarlayıcı. |
| [set_Instructions](./set_instructions/)(const System::String\&) | [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/) için ayarlayıcı. |
| [set_ShowDate](./set_showdate/)(bool) | [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/) için ayarlayıcı. |
| [set_Signer](./set_signer/)(const System::String\&) | İmza satırının önerilen imzalayanını ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Önerilen imzalayanın unvanını ayarlar. Bu özelliğin varsayılan değeri **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
