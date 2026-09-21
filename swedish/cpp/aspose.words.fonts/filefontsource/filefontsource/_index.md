---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource konstruktor"
linktitle: "FileFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource konstruktor. Konstruktor i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| filePath | const System::String\& | Sökväg till teckensnittsfilen. |

## Exempel



Visar hur man använder en typsnittfil i det lokala filsystemet som en typsnittskälla.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Se även

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| filePath | const System::String\& | Sökväg till teckensnittsfilen. |
| priority | int32_t | [Font](../../../aspose.words/font/) källprioritet. Se beskrivningen av egenskapen [Priority](../../fontsourcebase/get_priority/) för mer information. |

## Exempel



Visar hur man använder en typsnittfil i det lokala filsystemet som en typsnittskälla.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Se även

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


Konstruktör.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| filePath | const System::String\& | Sökväg till teckensnittsfilen. |
| priority | int32_t | [Font](../../../aspose.words/font/) källprioritet. Se beskrivningen av egenskapen [Priority](../../fontsourcebase/get_priority/) för mer information. |
| cacheKey | const System::String\& | Nyckeln för denna källa i cachen. Se [CacheKey](../get_cachekey/) egenskapsbeskrivning för mer information. |

## Se även

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
