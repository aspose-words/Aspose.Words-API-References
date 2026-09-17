---
title: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructeur"
linktitle: "OdtSaveOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions constructeur. Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format Odt en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions::OdtSaveOptions() constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Odt](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions()
```


## Exemples



Montre comment faire en sorte qu'un document enregistré se conforme à un schéma ODT plus ancien.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Voir aussi

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat) constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Odt](../../../aspose.words/saveformat/) ou [Ott](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | Peut être [Odt](../../../aspose.words/saveformat/) ou [Ott](../../../aspose.words/saveformat/). |

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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OdtSaveOptions::OdtSaveOptions(const System::String\&) constructor


Initialise une nouvelle instance de cette classe qui peut être utilisée pour enregistrer un document au format [Odt](../../../aspose.words/saveformat/) chiffré avec un mot de passe.

```cpp
Aspose::Words::Saving::OdtSaveOptions::OdtSaveOptions(const System::String &password)
```

## Voir aussi

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
