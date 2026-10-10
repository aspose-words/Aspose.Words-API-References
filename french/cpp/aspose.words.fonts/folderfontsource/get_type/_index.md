---
title: "Aspose::Words::Fonts::FolderFontSource::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FolderFontSource::get_Type méthode. Renvoie le type de la source de police en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


Renvoie le type de la source de police.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
