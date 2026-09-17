---
title: "Aspose::Words::SignatureLineOptions class"
linktitle: "SignatureLineOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::SignatureLineOptions class. Permet de spécifier les options pour la ligne de signature insérée. Utilisé dans DocumentBuilder. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 61000
url: /fr/cpp/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class


Permet de spécifier les options pour la ligne de signature insérée. Utilisé dans [DocumentBuilder](../documentbuilder/). Pour en savoir plus, consultez l'article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class SignatureLineOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AllowComments](./get_allowcomments/)() const | Obtient ou définit une valeur indiquant que le signataire peut ajouter des commentaires dans la boîte de dialogue Sign. La valeur par défaut de cette propriété est **false**. |
| [get_DefaultInstructions](./get_defaultinstructions/)() const | Obtient ou définit une valeur indiquant que les instructions par défaut sont affichées dans la boîte de dialogue Sign. La valeur par défaut de cette propriété est **true**. |
| [get_Email](./get_email/)() const | Obtient ou définit l'adresse e‑mail du signataire suggéré. La valeur par défaut de cette propriété est **empty string**. |
| [get_Instructions](./get_instructions/)() const | Obtient ou définit les instructions destinées au signataire qui sont affichées lors de la signature de la ligne de signature. La valeur par défaut de cette propriété est **empty string**. |
| [get_ShowDate](./get_showdate/)() const | Obtient ou définit une valeur indiquant que la date de signature est affichée dans la ligne de signature. La valeur par défaut de cette propriété est **true**. |
| [get_Signer](./get_signer/)() const | Obtient le signataire suggéré de la ligne de signature. La valeur par défaut de cette propriété est **empty string**. |
| [get_SignerTitle](./get_signertitle/)() const | Obtient le titre du signataire suggéré. La valeur par défaut de cette propriété est **empty string**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowComments](./set_allowcomments/)(bool) | Définisseur pour [Aspose::Words::SignatureLineOptions::get_AllowComments](./get_allowcomments/). |
| [set_DefaultInstructions](./set_defaultinstructions/)(bool) | Définisseur pour [Aspose::Words::SignatureLineOptions::get_DefaultInstructions](./get_defaultinstructions/). |
| [set_Email](./set_email/)(const System::String\&) | Définisseur pour [Aspose::Words::SignatureLineOptions::get_Email](./get_email/). |
| [set_Instructions](./set_instructions/)(const System::String\&) | Définisseur pour [Aspose::Words::SignatureLineOptions::get_Instructions](./get_instructions/). |
| [set_ShowDate](./set_showdate/)(bool) | Définisseur pour [Aspose::Words::SignatureLineOptions::get_ShowDate](./get_showdate/). |
| [set_Signer](./set_signer/)(const System::String\&) | Définit le signataire suggéré de la ligne de signature. La valeur par défaut de cette propriété est **empty string**. |
| [set_SignerTitle](./set_signertitle/)(const System::String\&) | Définit le titre du signataire suggéré. La valeur par défaut de cette propriété est **empty string**. |
| [SignatureLineOptions](./signaturelineoptions/)() |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment signer un document avec un certificat personnel et une ligne de signature.
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

// Rouvrez notre document enregistré et vérifiez que les propriétés "IsSigned" et "IsValid" sont toutes deux égales à "true",
// indiquant que la ligne de signature contient une signature.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentBuilder.SignatureLineProviderId.Signed.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
signatureLine = shape->get_SignatureLine();

ASSERT_TRUE(signatureLine->get_IsSigned());
ASSERT_TRUE(signatureLine->get_IsValid());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
