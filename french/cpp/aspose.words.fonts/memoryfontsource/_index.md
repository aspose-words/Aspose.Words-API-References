---
title: "Aspose::Words::Fonts::MemoryFontSource classe"
linktitle: "MemoryFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::MemoryFontSource classe. Représente le fichier de police TrueType unique stocké en mémoire. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Représente le fichier de police TrueType unique stocké en mémoire. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La clé de cette source dans le cache. |
| [get_FontData](./get_fontdata/)() const | Données de police binaires. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Renvoie la priorité de la source de police. |
| [get_Type](./get_type/)() override | Renvoie le type de la source de police. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Constructeur. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Constructeur. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Constructeur. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| static [Type](./type/)() |  |

## Exemples



Montre comment utiliser un tableau d'octets contenant les données d'un fichier de police comme source de police.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Voir aussi

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
