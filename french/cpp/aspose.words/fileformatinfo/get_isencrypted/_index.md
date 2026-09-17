---
title: "Méthode Aspose::Words::FileFormatInfo::get_IsEncrypted"
linktitle: "get_IsEncrypted"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::FileFormatInfo::get_IsEncrypted. Retourne true si le document est chiffré et nécessite un mot de passe pour l'ouvrir en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/fileformatinfo/get_isencrypted/
---
## FileFormatInfo::get_IsEncrypted method


Renvoie **true** si le document est chiffré et nécessite un mot de passe pour être ouvert.

```cpp
bool Aspose::Words::FileFormatInfo::get_IsEncrypted() const
```

## Remarques


Cette propriété existe pour vous aider à trier les documents chiffrés de ceux qui ne le sont pas. Si vous essayez de charger un document chiffré avec Aspose.Words sans fournir de mot de passe, une exception sera levée. Vous pouvez utiliser cette propriété pour détecter si un document nécessite un mot de passe et prendre une mesure avant de charger le document, par exemple demander le mot de passe à l'utilisateur.

## Exemples



Montre comment utiliser la classe [FileFormatUtil](../../fileformatutil/) pour détecter le format du document et le chiffrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configurez un objet SaveOptions pour chiffrer le document
// avec un mot de passe lors de l'enregistrement, puis enregistrez le document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Vérifiez le type de fichier de notre document ainsi que son état de chiffrement.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```

## Voir aussi

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
