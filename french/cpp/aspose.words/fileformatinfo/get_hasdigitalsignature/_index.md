---
title: "Méthode Aspose::Words::FileFormatInfo::get_HasDigitalSignature"
linktitle: "get_HasDigitalSignature"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::FileFormatInfo::get_HasDigitalSignature. Retourne true si ce document contient une signature numérique. Cette propriété indique simplement qu'une signature numérique est présente sur un document, mais ne précise pas si la signature est valide ou non en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


Renvoie **true** si ce document contient une signature numérique. Cette propriété indique simplement qu'une signature numérique est présente sur un document, mais elle ne précise pas si la signature est valide ou non.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## Remarques


Cette propriété existe pour vous aider à trier les documents signés numériquement de ceux qui ne le sont pas. Si vous utilisez Aspose.Words pour modifier et enregistrer un document signé numériquement, la signature numérique sera perdue. C’est ainsi prévu, car une signature numérique sert à garantir l'authenticité d'un document. En utilisant cette propriété, vous pouvez détecter les documents signés numériquement avant de les traiter de la même manière que les documents normaux et prendre une mesure pour éviter de perdre la signature numérique, par exemple notifier l'utilisateur.

## Exemples



Montre comment utiliser la classe [FileFormatUtil](../../fileformatutil/) pour détecter le format du document et la présence de signatures numériques.
```cpp
// Utilisez une instance de FileFormatInfo pour vérifier qu'un document n'est pas signé numériquement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Utilisez une nouvelle FileFormatInstance pour confirmer qu'il est signé.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// Nous pouvons charger et accéder aux signatures d'un document signé dans une collection comme celle-ci.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## Voir aussi

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
