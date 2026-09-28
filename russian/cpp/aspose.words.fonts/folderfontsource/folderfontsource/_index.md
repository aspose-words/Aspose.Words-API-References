---
title: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource конструктор"
linktitle: "FolderFontSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FolderFontSource::FolderFontSource конструктор. Конструктор в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource::FolderFontSource(const System::String\&, bool) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | const System::String\& | Путь к папке. |
| scanSubfolders | bool | Определяет, следует ли сканировать подпапки. |

## Примеры



Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.
```cpp
// Создайте источник шрифтов из папки, содержащей файлы шрифтов.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## См. также

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FolderFontSource::FolderFontSource(const System::String\&, bool, int32_t) constructor


Конструктор.

```cpp
Aspose::Words::Fonts::FolderFontSource::FolderFontSource(const System::String &folderPath, bool scanSubfolders, int32_t priority)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | const System::String\& | Путь к папке. |
| scanSubfolders | bool | Определяет, следует ли сканировать подпапки. |
| priority | int32_t | [Font](../../../aspose.words/font/) приоритет источника. Смотрите описание свойства [Priority](../../fontsourcebase/get_priority/) для получения дополнительной информации. |

## Примеры



Показывает, как использовать локальную системную папку, содержащую шрифты, в качестве источника шрифтов.
```cpp
// Создайте источник шрифтов из папки, содержащей файлы шрифтов.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## См. также

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
