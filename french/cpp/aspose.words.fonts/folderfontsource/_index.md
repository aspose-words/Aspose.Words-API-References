---
title: "Aspose::Words::Fonts::FolderFontSource classe"
linktitle: "FolderFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FolderFontSource classe. Représente le dossier qui contient des fichiers de police TrueType. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Représente le dossier qui contient les fichiers de police TrueType. Pour en savoir plus, visitez l’article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Constructeur. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Constructeur. |
| [get_FolderPath](./get_folderpath/)() const | Chemin du dossier. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Renvoie la priorité de la source de police. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Détermine s'il faut ou non analyser les sous‑dossiers. |
| [get_Type](./get_type/)() override | Renvoie le type de la source de police. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| static [Type](./type/)() |  |

## Exemples



Montre comment utiliser un dossier système local contenant des polices comme source de police.
```cpp
// Créez une source de police à partir d'un dossier contenant des fichiers de police.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Voir aussi

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
