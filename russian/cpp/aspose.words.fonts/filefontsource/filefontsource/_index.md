---
title: "Aspose::Words::Fonts::FileFontSource::FileFontSource конструктор"
linktitle: "FileFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FileFontSource::FileFontSource конструктор. Конструктор в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fonts/filefontsource/filefontsource/
---
## FileFontSource::FileFontSource(const System::String\&) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | const System::String\& | Путь к файлу шрифта. |

## Примеры



Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## См. также

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | const System::String\& | Путь к файлу шрифта. |
| priority | int32_t | [Font](../../../aspose.words/font/) приоритет источника. Смотрите описание свойства [Priority](../../fontsourcebase/get_priority/) для получения дополнительной информации. |

## Примеры



Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## См. также

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FileFontSource::FileFontSource(const System::String\&, int32_t, const System::String\&) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::FileFontSource::FileFontSource(const System::String &filePath, int32_t priority, const System::String &cacheKey)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| filePath | const System::String\& | Путь к файлу шрифта. |
| priority | int32_t | [Font](../../../aspose.words/font/) приоритет источника. Смотрите описание свойства [Priority](../../fontsourcebase/get_priority/) для получения дополнительной информации. |
| cacheKey | const System::String\& | Ключ этого источника в кэше. См. описание свойства [CacheKey](../get_cachekey/) для получения дополнительной информации. |

## См. также

* Class [FileFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
