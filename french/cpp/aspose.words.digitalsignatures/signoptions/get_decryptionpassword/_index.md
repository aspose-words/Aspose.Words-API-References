---
title: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword méthode"
linktitle: "get_DecryptionPassword"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword méthode. Le mot de passe pour déchiffrer le document source. La valeur par défaut est une chaîne vide en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.digitalsignatures/signoptions/get_decryptionpassword/
---
## SignOptions::get_DecryptionPassword method


Le mot de passe pour déchiffrer le document source. La valeur par défaut est **empty string**.

```cpp
System::String Aspose::Words::DigitalSignatures::SignOptions::get_DecryptionPassword() const
```


## Exemples



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

* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
