---
title: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructeur"
linktitle: "MemoryFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource constructeur. Constructeur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/memoryfontsource/memoryfontsource/
---
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Données de police binaires. |

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

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Données de police binaires. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorité de la source. Voir la description de la propriété [Priority](../../fontsourcebase/get_priority/) pour plus d'informations. |

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

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## MemoryFontSource::MemoryFontSource(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::MemoryFontSource::MemoryFontSource(const System::ArrayPtr<uint8_t> &fontData, int32_t priority, const System::String &cacheKey)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fontData | const System::ArrayPtr\<uint8_t\>\& | Données de police binaires. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorité de la source. Voir la description de la propriété [Priority](../../fontsourcebase/get_priority/) pour plus d'informations. |
| cacheKey | const System::String\& | La clé de cette source dans le cache. Voir la description de la propriété [CacheKey](../get_cachekey/) pour plus d'informations. |

## Voir aussi

* Class [MemoryFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
