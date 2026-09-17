---
title: "Méthode Aspose::Words::Loading::LoadOptions::get_Password"
linktitle: "get_Password"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::LoadOptions::get_Password. Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être nul ou une chaîne vide. La valeur par défaut est null en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.loading/loadoptions/get_password/
---
## LoadOptions::get_Password method


Obtient ou définit le mot de passe pour ouvrir un document chiffré. Peut être **null** ou une chaîne vide. La valeur par défaut est **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_Password() const
```

## Remarques


Vous devez connaître le mot de passe pour ouvrir un document chiffré. Si le document n'est pas chiffré, définissez ceci sur **null** ou une chaîne vide.

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

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
