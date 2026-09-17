---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments méthode"
linktitle: "get_Comments"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_Comments méthode. Spécifie les commentaires sur la signature numérique. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.digitalsignatures/signoptions/get_comments/
---
## SignOptions::get_Comments method


Spécifie les commentaires sur la signature numérique. La valeur par défaut est **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_Comments() const
```


## Exemples



Montre comment signer numériquement des documents.
```cpp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Prenez un document non signé depuis le système de fichiers local via un flux de fichier,
// puis créez une copie signée déterminée par le nom de fichier du flux de sortie.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Voir aussi

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
