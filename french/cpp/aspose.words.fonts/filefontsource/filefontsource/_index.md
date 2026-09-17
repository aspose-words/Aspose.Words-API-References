---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource constructeur"
linktitle: "FileFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource constructeur. Constructeur en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| filePath | const System::String\& | Chemin vers le fichier de police. |

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
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| filePath | const System::String\& | Chemin vers le fichier de police. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorité de la source. Voir la description de la propriété [Priority](../../fontsourcebase/get_priority/) pour plus d'informations. |

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
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


Constructeur.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| filePath | const System::String\& | Chemin vers le fichier de police. |
| priority | int32_t | [Font](../../../aspose.words/font/) priorité de la source. Voir la description de la propriété [Priority](../../fontsourcebase/get_priority/) pour plus d'informations. |
| cacheKey | const System::String\& | La clé de cette source dans le cache. Voir la description de la propriété [CacheKey](../get_cachekey/) pour plus d'informations. |

## Voir aussi

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
