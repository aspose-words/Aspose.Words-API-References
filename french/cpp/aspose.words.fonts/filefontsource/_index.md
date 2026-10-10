---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FileFontSource class. Représente le fichier de police TrueType unique stocké dans le système de fichiers. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Représente le fichier de police TrueType unique stocké dans le système de fichiers. Pour en savoir plus, visitez l’article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Constructeur. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Constructeur. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Constructeur. |
| [get_CacheKey](./get_cachekey/)() const | La clé de cette source dans le cache. |
| [get_FilePath](./get_filepath/)() const | Chemin du fichier de police. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Renvoie la priorité de la source de police. |
| [get_Type](./get_type/)() override | Renvoie le type de la source de police. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
