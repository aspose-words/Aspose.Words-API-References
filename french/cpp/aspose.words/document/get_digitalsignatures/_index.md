---
title: "Aspose::Words::Document::get_DigitalSignatures méthode"
linktitle: "get_DigitalSignatures"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_DigitalSignatures méthode. Obtient la collection de signatures numériques pour ce document ainsi que leurs résultats de validation en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words/document/get_digitalsignatures/
---
## Document::get_DigitalSignatures method


Obtient la collection des signatures numériques de ce document et leurs résultats de validation.

```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::Document::get_DigitalSignatures() const
```

## Remarques


Cette collection contient les signatures numériques qui ont été chargées depuis le document original. Ces signatures numériques ne seront pas enregistrées lorsque vous enregistrez cet objet [Document](../) dans un fichier ou un flux, car l'enregistrement ou la conversion produira un document différent de l'original et les signatures numériques originales ne seront plus valides.

Cette collection n'est jamais **null**. Si le document n'est pas signé, elle contiendra zéro élément.

## Exemples



Montre comment valider et afficher les informations sur chaque signature dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```


Montre comment signer des documents avec des certificats X.509.
```cpp
// Vérifiez qu'un document n'est pas signé.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Créez un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Il existe deux façons d'enregistrer une copie signée d'un document sur le système de fichiers local :
// 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Prenez un document depuis un flux et enregistrez une copie signée dans un autre flux.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Veuillez vérifier que toutes les signatures numériques du document sont valides et consulter leurs détails.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Voir aussi

* Class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
