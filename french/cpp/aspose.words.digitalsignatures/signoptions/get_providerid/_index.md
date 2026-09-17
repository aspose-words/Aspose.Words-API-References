---
title: "Méthode Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId"
linktitle: "get_ProviderId"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId. Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est Empty (tous les zéros) Guid en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.digitalsignatures/signoptions/get_providerid/
---
## SignOptions::get_ProviderId method


Spécifie l'ID de classe du fournisseur de signature. La valeur par défaut est **Empty (all zeroes) Guid**.

```cpp
System::Guid Aspose::Words::DigitalSignatures::SignOptions::get_ProviderId() const
```

## Remarques


Le fournisseur de services cryptographiques (CSP) est un module logiciel indépendant qui exécute réellement les algorithmes de cryptographie pour l'authentification, le codage et le chiffrement. MS Office réserve la valeur {00000000-0000-0000-0000-000000000000} pour son fournisseur de signature par défaut.

Le GUID du fournisseur installé supplémentaire doit être obtenu à partir de la documentation fournie avec le fournisseur.

De plus, tous les fournisseurs cryptographiques installés sont répertoriés dans le registre Windows. Ils se trouvent dans le chemin suivant : HKLM\SOFTWARE\**Microsoft**\Cryptography\Defaults\Provider. Il existe une clé nommée "CP Service UUID" qui correspond à un GUID de fournisseur de signature.

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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
