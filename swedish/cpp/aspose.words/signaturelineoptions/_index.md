---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::SignatureLineOptions-klass. Tillåter att ange alternativ för signaturlinje som infogas. Används i DocumentBuilder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 61000
url: /sv/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Tillåter att ange alternativ för signaturlinje som infogas. Används i [DocumentBuilder](../documentbuilder/). För att lära dig mer, besök dokumentationsartikeln [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Hämtar eller anger ett värde som indikerar att undertecknaren kan lägga till kommentarer i Sign-dialogen. Standardvärdet för denna egenskap är **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Hämtar eller anger ett värde som indikerar att standardinstruktioner visas i Sign-dialogen. Standardvärdet för denna egenskap är **true**. |
| [get_Email](./get_email/)() const | Hämtar eller anger föreslagen undertecknares e‑postadress. Standardvärdet för denna egenskap är **empty string**. |
| [get_Instructions](./get_instructions/)() const | Hämtar eller anger instruktioner till undertecknaren som visas vid signering av signaturlinjen. Standardvärdet för denna egenskap är **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Hämtar eller anger ett värde som indikerar att signeringsdatum visas i signaturlinjen. Standardvärdet för denna egenskap är **true**. |
| [get_Signer](./get_signer/)() const | Hämtar föreslagen undertecknare för signaturlinjen. Standardvärdet för denna egenskap är **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Hämtar föreslagen undertecknares titel. Standardvärdet för denna egenskap är **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Sättare för [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Sättare för [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Sättare för [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Sättare för [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Sättare för [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Anger föreslagen undertecknare för signaturlinjen. Standardvärdet för denna egenskap är **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Anger föreslagen undertecknares titel. Standardvärdet för denna egenskap är **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man signerar ett dokument med ett personligt certifikat och en signaturlinje.
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

// Öppna vårt sparade dokument igen och verifiera att egenskaperna \"IsSigned\" och \"IsValid\" båda är lika med \"true\",
// vilket indikerar att signaturlinjen innehåller en signatur.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
