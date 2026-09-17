---
title: "Aspose::Words::Saving::OdtSaveOptions::get_Password méthode"
linktitle: "get_Password"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_Password méthode. Obtient ou définit un mot de passe pour chiffrer le document en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/odtsaveoptions/get_password/
---
## OdtSaveOptions::get_Password method


Obtient ou définit un mot de passe pour chiffrer le document.

```cpp
System::String Aspose::Words::Saving::OdtSaveOptions::get_Password() const
```

## Remarques


Afin d'enregistrer le document sans chiffrement, cette propriété doit être **null** ou une chaîne vide.

## Exemples



Montre comment chiffrer un document ODT/OTT enregistré avec un mot de passe, puis le charger en utilisant Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Créez une nouvelle OdtSaveOptions et transmettez soit "SaveFormat.Odt",
// ou "SaveFormat.Ott" comme format pour enregistrer le document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(saveFormat);
saveOptions->set_Password(u"@sposeEncrypted_1145");

System::String extensionString = Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat);

// Si nous ouvrons ce document avec un éditeur approprié,
// il nous demandera le mot de passe que nous avons spécifié dans l'objet SaveOptions.
doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, saveOptions);

System::SharedPtr<Aspose::Words::FileFormatInfo> docInfo = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString);

ASSERT_TRUE(docInfo->get_IsEncrypted());

// Si nous souhaitons ouvrir ou modifier à nouveau ce document en utilisant Aspose.Words,
// nous devrons fournir un objet LoadOptions contenant le mot de passe correct au constructeur de chargement.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Encrypt" + extensionString, System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"@sposeEncrypted_1145"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
