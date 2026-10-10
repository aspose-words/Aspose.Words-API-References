---
title: "Aspose::Words::DigitalSignatures::CertificateHolder class"
linktitle: "CertificateHolder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::CertificateHolder class. Représente un détenteur d'une instance X509Certificate2. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class


Représente un détenteur d’une instance **X509Certificate2**. Pour en savoir plus, consultez l’article de documentation [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class CertificateHolder : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<System::Security::SecureString\>\&) | Crée l'objet [CertificateHolder](./) en utilisant le tableau d'octets du magasin PKCS12 et son mot de passe. |
| static [Create](./create/)(const System::ArrayPtr\<uint8_t\>\&, const System::String\&) | Crée l'objet [CertificateHolder](./) en utilisant le tableau d'octets du magasin PKCS12 et son mot de passe. |
| static [Create](./create/)(const System::String\&, const System::String\&) | Crée l'objet [CertificateHolder](./) en utilisant le chemin du magasin PKCS12 et son mot de passe. |
| static [Create](./create/)(const System::String\&, const System::String\&, const System::String\&) | Crée l'objet [CertificateHolder](./) en utilisant le chemin du magasin PKCS12, son mot de passe et l'alias permettant de trouver la clé privée et le certificat. |
| [get_Certificate](./get_certificate/)() | Renvoie l'instance de **X509Certificate2** qui contient les clés privées, publiques et la chaîne de certificats. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Remarques


[CertificateHolder](./) can be created by static factory methods only. It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system. This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with **X509Certificate2** as parameters.

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


Montre comment signer un fichier de document chiffré.
```cpp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Créez un commentaire, une date et un mot de passe de déchiffrement qui seront appliqués avec notre nouvelle signature numérique.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

// Définissez un nom de fichier système local pour le document d'entrée non signé, et un nom de fichier de sortie pour sa nouvelle copie signée numériquement.
System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.DecryptionPassword.docx";

Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Voir aussi

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
