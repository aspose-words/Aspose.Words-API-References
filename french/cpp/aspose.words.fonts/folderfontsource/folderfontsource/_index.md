---
title: "Constructeur Aspose::Words::Fonts::FolderFontSource::FolderFontSource"
linktitle: "FolderFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Constructeur Aspose::Words::Fonts::FolderFontSource::FolderFontSource. Ctor en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| folderPath | const System::String\& | Chemin vers le dossier. |
| scanSubfolders | bool | Détermine s'il faut ou non analyser les sous-dossiers. |

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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| folderPath | const System::String\& | Chemin vers le dossier. |
| scanSubfolders | bool | Détermine s'il faut ou non analyser les sous-dossiers. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorité de la source. Voir la description de la propriété [Priority](../../fontsourcebase/get_priority/) pour plus d'informations. |

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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
