---
title: "Aspose::Words::Fonts::FontSourceType énum"
linktitle: "FontSourceType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSourceType enum. Spécifie le type de source de police en C++."
type: docs
weight: 23000
url: /fr/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Spécifie le type de source de police.

```cpp
enum class FontSourceType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| FontFile | 0 | Un objet [FileFontSource](../filefontsource/) qui représente un fichier de police unique. |
| FontsFolder | 1 | Un objet [FolderFontSource](../folderfontsource/) qui représente un dossier contenant des fichiers de police. |
| MemoryFont | 2 | Un objet [MemoryFontSource](../memoryfontsource/) qui représente une police unique en mémoire. |
| SystemFonts | 3 | Un objet [SystemFontSource](../systemfontsource/) qui représente toutes les polices installées sur le système. |
| FontStream | 4 | Un objet [StreamFontSource](../streamfontsource/) qui représente un flux contenant des données de police. |


## Exemples



Montre comment utiliser un fichier de police dans le système de fichiers local comme source de police.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
