---
title: "Aspose::Words::Fonts::FileFontSource::get_FilePath méthode"
linktitle: "get_FilePath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FileFontSource::get_FilePath méthode. Chemin vers le fichier de police en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fonts/filefontsource/get_filepath/
---
## FileFontSource::get_FilePath method


Chemin du fichier de police.

```cpp
System::String Aspose::Words::Fonts::FileFontSource::get_FilePath() const
```


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

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
