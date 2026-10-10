---
title: "Aspose::Words::Fonts::FileFontSource::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FileFontSource::get_Type méthode. Retourne le type de la source de police en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.fonts/filefontsource/get_type/
---
## FileFontSource::get_Type method


Renvoie le type de la source de police.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FileFontSource::get_Type() override
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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
